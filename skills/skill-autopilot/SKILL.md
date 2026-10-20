---
name: skill-autopilot
description: Autonomous skill acquisition and run loop. Reads the user's goal for the CURRENT project, uses the skills ecosystem (find-skills / `npx skills`) to discover the skill the project needs, installs the best match automatically, then runs the project using it. Use when the user describes a goal or a project and wants the right skill found, installed, and put to work WITHOUT having to name the skill or run install commands by hand. Triggers on "/autopilot", "find and install the skill I need and run this", "faça o que precisa pra esse projeto", "descubra a skill certa, instale e rode", "set this project up end to end".
user_invocable: true
---

# Skill Autopilot

The autonomous counterpart to `find-skills`. Where `find-skills` waits for the user
to point it at a query and confirm each install, **autopilot** reads the goal, decides
what capability is missing, acquires it, and uses it — in one pass, stopping only when
a decision is genuinely the user's to make.

Pipeline: **understand → discover → install → load → run → report.**

## When to use

Use this when the user:
- Describes what they want built/done and expects you to figure out the tooling.
- Says "find the skill I need, install it, and run the project" (any language).
- Invokes `/autopilot [goal]`.

Do **not** use it for a one-off question you can answer directly, or when the user
already named a specific skill (just install that one).

## The pipeline

### 1. Understand the goal and the project
- Take the user's stated goal. If `/autopilot` was called with an argument, that
  argument IS the goal.
- Inspect the current working directory to characterize the project: read
  `package.json` / `pyproject.toml` / `Cargo.toml` / `go.mod` / `README`, and the
  file tree. Derive: language, framework, and the task domain (testing, deploy,
  design, data, security, docs, …).
- Produce a one-line **capability query**, e.g. "next.js e2e testing" or
  "rust cli release packaging". This is what you'll search for.

### 2. Discover candidate skills
Search the open skills ecosystem (this is what `find-skills` drives):

```bash
npx -y skills find "<capability query>"
```

- Also consider already-installed skills first (`npx -y skills list`) and the
  skills.sh leaderboard — do not reinstall something already present.
- Pick the single best match by relevance to the query and popularity. If two are
  close, prefer the more-installed / better-documented one.

### 3. Install automatically
Install globally, for Claude Code, non-interactively:

```bash
npx -y skills add <owner/repo> --skill <name> -a claude-code -g -y
```

- `-y` skips confirmation, `-g` makes it available across projects, `-a claude-code`
  targets this agent. Installed skills land in `~/.claude/skills/` and load on the
  **next** session — so after installing, read the new `SKILL.md` directly and follow
  it now rather than waiting for a restart.
- If `npx skills find` returns nothing usable, say so and offer to scaffold one with
  `npx -y skills init <name>` instead of guessing.

### 4. Load and run the project
- Read the newly installed skill's `SKILL.md` and apply its instructions to the goal.
- Then actually run the project. Prefer a project-specific launch skill if one exists;
  otherwise fall back to the built-in `run` skill (`Skill(run)`), or the obvious
  command for the stack (`npm run dev`/`test`, `cargo run`, `pytest`, etc.).
- Capture real output. Report what the skill was, what it did, and the actual result —
  never claim success you didn't observe.

### 5. Report
Give the user a short summary: capability query → skill chosen → install result →
run result. Name the skill and link its source.

## Guardrails
- **Confirm before anything hard to reverse or outward-facing:** deploying, publishing,
  pushing, deleting, spending money, or sending data to an external service. Discovery,
  install, and a local build/test run are fine to do autonomously.
- One capability at a time. If the goal needs several skills, loop this pipeline per
  capability rather than installing a pile at once.
- Never install a skill whose `SKILL.md` you have not read, and never run a bundled
  script from it without looking at what it does first.
- If install or run fails, report the failure and the output — do not retry blindly.

## Relationship to find-skills
`find-skills` = user-driven discovery + install, with confirmation.
`skill-autopilot` = goal-driven, chains discovery → install → run with minimal stops.
They share the same `npx skills` backend, so anything autopilot installs is visible to
`find-skills` and vice-versa.
