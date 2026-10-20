# all-skills-in-one

> **Uma única skill que contém todas as outras.** 126 skills reunidas em um só pacote, compatível com
> **Claude Code, OpenAI Codex, Cursor e Gemini CLI** e qualquer agente que leia o formato `SKILL.md`.

Cada skill mantém seu próprio `skills/<nome>/SKILL.md` e continua acionável individualmente.

> As skills de segurança ofensiva (cibersegurança/pentest) foram removidas desta coleção pública por segurança.

## Instalação

### Claude Code (como plugin)
```bash
claude plugin marketplace add godnexusia-sketch/all-skills-in-one
claude plugin install all-skills-in-one@all-skills-in-one
```
Ou: `cp -r skills/* ~/.claude/skills/`

### Codex / Cursor / Gemini CLI e outros
```bash
npx -y skills add godnexusia-sketch/all-skills-in-one -a '*' -g -y
```

## Índice completo (126 skills)

- **access** — responsável por Manage Discord channel access — approve pairings, edit allowlists, set DM/group policy.
- **Agent Cost Report** — responsável por - Believable agent cost report for any period, default the last 7 full days PT, not counting today.
- **agent-development** — responsável por This skill should be used when the user asks to "create an agent", "add an agent", "write a subagent", "agent frontmatter", "when to use description", "agent examples", "agent tools", "agent colors", "autonomous agent...
- **babysit** — responsável por Watch a pull request or review cycle until it is ready to merge.
- **brag** — responsável por Memorialize something you just built by generating a self-contained "showcase" page for it — a persuasive, good-looking deep dive: what it is, why it's impressive, how it works — with a screenshot if one can be found...
- **brainstorming** — responsável por You MUST use this before any creative work - creating features, building components, adding functionality, modifying behavior, or planning anything new, in software or out of it (a talk, a business, a renovation).
- **branch** — responsável por Create an isolated git worktree for a task and log it to a shared work journal, so multiple Claude Code sessions run in parallel without racing on HEAD, uncommitted edits, or the index.
- **build** — responsável por Fully automate a coding task with make-plan, do, and babysit.
- **build-and-release** — responsável por Fully automate building and releasing a coding task.
- **build-mcp-app** — responsável por This skill should be used when the user wants to build an "MCP app", add "interactive UI" or "widgets" to an MCP server, "render components in chat", build "MCP UI resources", make a tool that shows a "form", "picker"...
- **build-mcp-server** — responsável por This skill should be used when the user asks to "build an MCP server", "create an MCP", "make an MCP integration", "wrap an API for Claude", "expose tools to Claude", "make an MCP app", or discusses building something...
- **build-mcpb** — responsável por This skill should be used when the user wants to "package an MCP server", "bundle an MCP", "make an MCPB", "ship a local MCP server", "distribute a local MCP", discusses ".mcpb files", mentions bundling a Node or Pyth...
- **built-in-browser** — responsável por Read this skill before the first step that uses the built-in browser, the browser pane inside the Claude desktop app (also called the in-app browser, the browser pane, Claude's browser, or \"your own browser\"), whose...
- **cardputer-buddy** — responsável por Iterate on the Cardputer-Adv MicroPython app bundle (Claude Buddy, Snake, Hello) after the device is already provisioned via m5-onboard.
- **ccs-align** — responsável por Run the CCS Align seat's hourly breathing cycle — prove the local claude-mem worker is healthy, pull needle observations through search → timeline → get_observations, land them in a seat-owned middle cache via atomic...
- **childhood** — responsável por Babysit a shipped release after merge, publication, or deployment.
- **chrome-browser** — responsável por Read this skill before the first step that uses Claude in Chrome, the browser extension whose tools are named mcp__claude-in-chrome__* (also called Chrome, the browser extension, or the external browser) and which act...
- **claude-automation-recommender** — responsável por Analyze a codebase and recommend Claude Code automations (hooks, subagents, skills, plugins, MCP servers).
- **claude-code-best-practices** — responsável por Use when asked about Claude Code workflow, prompt caching cost, session economics, CLAUDE.md hygiene, context-window management, plan mode, permission modes, hooks, skills, subagents, checkpointing/rewind, parallel se...
- **claude-md-improver** — responsável por Audit and improve CLAUDE.md files in repositories.
- **claude-security** — responsável por Claude Security: scan the codebase (the whole repository or a scoped part of it), scan changes (this branch's or a pull request's diff, or one commit), or suggest patches (findings turned into targeted patch files, ea...
- **cloud-sync** — responsável por Set up or check claude-mem cloud sync with cmem.ai Pro.
- **codebase-memory** — responsável por Use the codebase knowledge graph for structural code queries.
- **codex** — responsável por Delegate a task or question to the OpenAI Codex CLI running as an isolated subagent, then relay its answer.
- **codex-review** — responsável por | Get a second opinion on the current change or a plan from a different model (Codex), and enforce its verdict mechanically.
- **command-development** — responsável por This skill should be used when the user asks to "create a slash command", "add a command", "write a custom command", "define command arguments", "use command frontmatter", "organize commands", "create command with fil...
- **comment-refactor** — responsável por Refactor the comments in AI-generated (or long-lived) code — strip the accumulation of fix-history narration, obsolete explanations, and code-restating noise while preserving load-bearing WHY/TODO/warning comments.
- **computer-use** — responsável por Read this skill before the first step of any request to do something in an app on the person's own computer (Notes, Finder, System Settings, any desktop app), to look at their screen, or for \"computer use\".
- **configure** — responsável por Set up the Discord channel — save the bot token and review access policy.
- **context7-cli** — responsável por Use the ctx7 CLI to fetch library documentation and configure Context7 MCP.
- **context7-mcp** — responsável por This skill should be used when the user asks about libraries, frameworks, API references, or needs code examples.
- **crisp** — responsável por Use this skill when the user wants shorter, more direct responses.
- **curate** — responsável por Verify a session's or handoff's factual claims against ground truth before trusting them.
- **deep-research** — responsável por Use this skill when the user's prompt requires (1) researching a topic across multiple sources, comparing options or alternatives, analyzing trends or history, understanding markets or industries, or reviewing literat...
- **design-is** — responsável por Audit a design against Dieter Rams' ten "Good design is..." principles, then hand off a /make-plan prompt for one of three outcomes — new design, refine design, or redesign.
- **diagnosing-superpowers** — responsável por Use when a superpowers session went wrong and your human partner wants to know why — repeated work, ignored plans, stumbles, poor results, a skill that didn't fire, "it took too long", "why is it so expensive", "what...
- **dispatching-parallel-agents** — responsável por Use when facing 2+ independent tasks that can be worked on without shared state or sequential dependencies
- **do** — responsável por Execute a phased implementation plan using subagents.
- **docs** — responsável por docs (editable docs people share and comment on; the default for any document, named as a doc or not: a document, report, proposal, resume, cover letter, letter, contract, policy, form, template, worksheet, essay, han...
- **docx** — responsável por Use this skill whenever the user wants to create, read, edit, or manipulate Word documents (.docx) or Word templates (.dotx).
- **evaluate** — responsável por | Tear down a third-party product/tool/library from a single URL and answer two questions: (1) is the product worth adopting as-is — installed into your Claude Code workflow (a CLI, MCP server, skill, or dotfile) or o...
- **example-command** — responsável por An example user-invoked skill that demonstrates frontmatter options and the skills/<name>/SKILL.md layout
- **example-skill** — responsável por This skill should be used when the user asks to "demonstrate skills", "show skill format", "create a skill template", or discusses skill development patterns.
- **executing-plans** — responsável por Use when executing an implementation plan in the current session as the implementer yourself — your human partner chose inline execution, or no subagent tool is available
- **find-docs** — responsável por - Retrieves up-to-date documentation, API references, and code examples for any developer technology.
- **find-skills** — responsável por Helps users discover and install agent skills when they ask questions like "how do I do X", "find a skill for X", "is there a skill that can...", or express interest in extending capabilities.
- **finishing-a-development-branch** — responsável por Use when implementation is complete, all tests pass, and you need to decide how to integrate the work
- **fix-issue** — responsável por | Take a GitHub issue and actually resolve it end to end — read the issue, reproduce it, fix it in an isolated branch with a test, verify, and open a PR that closes the issue.
- **frontend-design** — responsável por Guidance for distinctive, intentional visual design when building new UI or reshaping an existing one.
- **frontier-spend** — responsável por Use when planning how to spend scarce or expiring access to a premium frontier-tier model (usage-capped, deprecation cliff, "how should I spend my remaining premium-model budget", 2x burn rate, model leaving the plan)...
- **gemini-review** — responsável por Get a second-opinion review of the current diff (or a chosen focus — architecture, security, docs, design, performance, tests) from the Gemini CLI, then present its findings alongside your own analysis.
- **get-reddit** — responsável por Fetch a specific public Reddit post (title, body, and top comments) as clean markdown, by driving a real browser session (Playwright) — because Reddit 403s all non-browser fetches AND closed self-serve API access in N...
- **github-review** — responsável por | Review a GitHub pull request — the PR-review behavior that used to live in the built-in `/review`, split out now that `/review` is the review orchestrator.
- **google-workspace** — responsável por Read this before the first Google Drive, Docs, Sheets or Slides connector call whenever the task creates or changes a Google file.
- **handoff** — responsável por Write a rich session handoff to a pause-*.md file — checklist, decisions, files changed, self-critique, and a verbatim-id "coordinate closet" — so a fresh session can resume the work after /clear (via the auto-resume...
- **hook-development** — responsável por This skill should be used when the user asks to "create a hook", "add a PreToolUse/PostToolUse/Stop hook", "validate tool use", "implement prompt-based hooks", "use ${CLAUDE_PLUGIN_ROOT}", "set up event-driven automat...
- **how-it-works** — responsável por Explain how claude-mem captures observations, when memory injection kicks in, and where data lives.
- **idea** — responsável por | Capture a fix / feature / research idea fast and turn it into a tracked GitHub Issue plus a lightweight planning doc, so nothing gets lost and it shows up next time you list your issues.
- **impeccable** — responsável por Use when the user wants to design, redesign, shape, critique, audit, polish, simplify, harden, animate, or otherwise improve a frontend interface: websites, landing pages, dashboards, product UI, components, forms, se...
- **import-memory** — responsável por Import a memory export from another AI assistant into Claude's memory — conversationally, additively, and with the content treated as data.
- **knowledge-agent** — responsável por Build and query AI-powered knowledge bases from claude-mem observations.
- **learn-codebase** — responsável por Prime a codebase by reading every source file in full.
- **llm-tools** — responsável por Use when a session is about to bulk-read 3+ files or any single file over ~400 lines, generate predictable boilerplate (tests, fixtures, config scaffolds, doc templates), or compress a long session transcript — and a...
- **m5-onboard** — responsável por End-to-end onboarding for a freshly-plugged-in M5Stack ESP32 device (Cardputer, Cardputer-Adv, Core, CoreS3, Stick) — detect on USB, flash UIFlow 2.0 firmware, and install the Claude Buddy MicroPython app bundle.
- **make-plan** — responsável por Create a detailed, phased implementation plan with documentation discovery.
- **math-olympiad** — responsável por Solve competition math problems (IMO, Putnam, USAMO, AIME) with adversarial verification that catches the errors self-verification misses.
- **mcp-integration** — responsável por This skill should be used when the user asks to "add MCP server", "integrate MCP", "configure MCP in plugin", "use .mcp.json", "set up Model Context Protocol", "connect external service", mentions "${CLAUDE_PLUGIN_ROO...
- **mem-search** — responsável por Search claude-mem persistent cross-session memory through enforced progressive disclosure.
- **mock** — responsável por | Quickly mock up alternative UI / interface designs as a single self-contained HTML file with a built-in view-switcher across variations, then hand it over: download the file, attach it to an email draft, or (if you...
- **mode-creator** — responsável por Interactively create, install, activate, and verify custom claude-mem modes, including domain-specific observation types, concept tags, optional Telegram alerts, bot setup, worker restart, and startup-context verifica...
- **morning** — responsável por Render the user's morning brief as a styled HTML artifact, or set it up as a recurring weekday task.
- **oh-my-issues** — responsável por Cluster a GitHub issue backlog by root cause into a small set of plan-master issues, redirect children with a standardized comment, and bundle architectural-fix PRs that close clusters atomically.
- **pathfinder** — responsável por Map a codebase into feature-grouped flowcharts, identify duplicated concerns across features, and propose a unified architecture.
- **pdf** — responsável por Use this skill whenever the user wants to do anything with PDF files.
- **persona-test** — responsável por | Run persona-based subagent tests against a target app through an app-specific adapter.
- **pickup** — responsável por Use when the user wants to pick up / resume the most recent handoff in an isolated worktree — finds the newest handoff doc, RESUMES the worktree/branch it documents if one exists (re-adding it if parked), otherwise cr...
- **playground** — responsável por Creates interactive HTML playgrounds — self-contained single-file explorers that let users configure something visually through controls, see a live preview, and copy out a prompt.
- **plugin-settings** — responsável por This skill should be used when the user asks about "plugin settings", "store plugin configuration", "user-configurable plugin", ".local.md files", "plugin state files", "read YAML frontmatter", "per-project plugin set...
- **plugin-structure** — responsável por This skill should be used when the user asks to "create a plugin", "scaffold a plugin", "understand plugin structure", "organize plugin components", "set up plugin.json", "use ${CLAUDE_PLUGIN_ROOT}", "add commands/age...
- **pptx** — responsável por Use this skill any time a .pptx or .potx file is involved in any way — as input, output, or both.
- **project-artifact** — responsável por Generate and publish a project status artifact — an opinionated, tabbed status page for a project too big for one update (overview & success criteria, the workstream sequence, next steps, plus background, plan, risks...
- **rea-analysis-optimization** — responsável por Optimize REA providers and shared analysis workflows for agent context, latency, CPU, and memory while preserving correctness and Evidence.
- **rea-changelog-update** — responsável por Prepare or rewrite REA release changelogs and GitHub release notes from pinned Git history, with verified contributor thanks and Release Please synchronization.
- **rea-ci-tests-audit** — responsável por Audit REA CI and test suites for correctness, fixture drift, false passes, and measured performance; use for suite or workflow investigations and efficiency changes, rather than ordinary feature testing or a single te...
- **rea-tool-design** — responsável por Design or change REA investigation tools, CLI/MCP contracts, provider capabilities, and Evidence semantics.
- **receipts** — responsável por Generate a personal Claude Code usage & impact report ("receipts") from this machine's local session transcripts — for justifying Claude Code usage/spend to a manager, self-review, or "what have I been using this for"...
- **receiving-code-review** — responsável por Use when receiving code review feedback, before implementing suggestions, especially if feedback seems unclear or technically questionable - requires technical rigor and verification, not performative agreement or bli...
- **release** — responsável por Fully automate a release with version-bump and childhood.
- **requesting-code-review** — responsável por Use when completing tasks, implementing major features, or before merging to verify work meets requirements
- **reverse-engineer-anything** — responsável por Reverse engineer native, managed, Electron/JavaScript, packaged, firmware, and browser targets with REA.
- **review** — responsável por | The top-level review verb — decide WHETHER, WHEN, WHICH, and HOW HARD to review a change before reaching for a review tool.
- **review-panel** — responsável por Run multiple independent code reviewers (Codex + Gemini + a fresh Claude) on the current diff or a plan, merge their structured verdicts, and apply a consensus-gated challenge round — returning a pass/fail exit code.
- **screenpipe** — responsável por Search screen and audio history recorded by Screenpipe and optionally save selected context into claude-mem.
- **session-end** — responsável por Wrap up a coding session — run a right-sized end-of-session self-critique, optionally curator-verify the claims, prepend a SESSION_LOG.md entry, and print a rename + counter summary.
- **session-pause** — responsável por Write a detailed session handoff file by hand so the next session can pick up where this one left off.
- **session-report** — responsável por Generate an explorable HTML report of Claude Code session usage (tokens, cache, subagents, skills, expensive prompts) from ~/.claude/projects transcripts.
- **session-resume** — responsável por Load a session handoff file and resume the work it describes.
- **session-start** — responsável por Begin a documented coding session — create a per-session log so progress is tracked and later wrap-up (/session-end) has something to append to.
- **siege** — responsável por Work on one hard mathematics problem in rounds: each round a judge writes a few self-contained questions, independent workers answer them, and the judge keeps a ledger of what is proved, refuted and open, until the ju...
- **sitrep** — responsável por Use when the user invokes /sitrep — an occasional "state of the union" re-orientation sweep.
- **skill-autopilot** — responsável por Autonomous skill acquisition and run loop.
- **skill-creator** — responsável por Create new skills, modify and improve existing skills, and measure skill performance.
- **skill-development** — responsável por This skill should be used when the user wants to "create a skill", "add a skill to plugin", "write a new skill", "improve skill description", "organize skill content", or needs guidance on skill structure, progressive...
- **smart-explore** — responsável por Token-optimized structural code search using tree-sitter AST parsing.
- **solo** — responsável por Work on one hard mathematics problem in this session yourself, with no sub-agents: reason in stages, record each settled step in a notes file so that nothing written is lost if a response is cut off, and end with a se...
- **standup** — responsável por Facilitate a read-only standup across git worktrees, branches, or PRs to compare changes and produce one consolidation plan.
- **startup-hook-skill** — responsável por Creating and developing startup hooks for Claude Code cloud sessions.
- **subagent-driven-development** — responsável por Use when executing implementation plans with independent tasks in the current session
- **sweep** — responsável por Use when work may have been dropped between sessions — after a crash, a lockup, parallel-session churn, or on a "did we drop anything?" hunch.
- **systematic-debugging** — responsável por Use when encountering any bug, test failure, or unexpected behavior, before proposing fixes
- **task-observer** — responsável por Monitors task execution for skill improvement opportunities.
- **test-driven-development** — responsável por Use when implementing any feature or bugfix, before writing implementation code
- **timeline-report** — responsável por Generate a "Journey Into [Project]" narrative report analyzing a project's entire development history from claude-mem's timeline.
- **unslop-ui** — responsável por - Detects and removes the visual patterns that make a website look AI-generated or "vibe-coded": the default shadcn/Tailwind look, AI-purple gradients, Inter/Geist fonts, unprompted neon glow, emoji used as icons, the...
- **using-git-worktrees** — responsável por Use when starting feature work that needs isolation from current workspace or before executing implementation plans - ensures an isolated workspace exists via native tools or git worktree fallback
- **using-superpowers** — responsável por Use when starting any conversation - establishes how to find and use skills, requiring skill invocation before ANY response including clarifying questions
- **verification-before-completion** — responsável por Use when about to claim work is complete, fixed, or passing, before committing or creating PRs - requires running verification commands and confirming output before making any success claims; evidence before assertion...
- **version-bump** — responsável por Automated semantic versioning and release workflow for Claude Code plugins.
- **weekly-digests** — responsável por Generate a serial week-by-week narrative digest of a project's full claude-mem timeline.
- **what-the** — responsável por What the?
- **wowerpoint** — responsável por Turn one document into a kawaii NotebookLM slide deck.
- **write-post** — responsável por | Turn a rough brief into a blog deep-dive draft.
- **writing-hookify-rules** — responsável por This skill should be used when the user asks to "create a hookify rule", "write a hook rule", "configure hookify", "add a hookify rule", or needs guidance on hookify rule syntax and patterns.
- **writing-plans** — responsável por Use when you have a spec or requirements for a multi-step task, before touching code
- **writing-skills** — responsável por Use when creating new skills, editing existing skills, or verifying skills work before deployment
- **xlsx** — responsável por Use this skill any time a spreadsheet file is the primary input or output.

## Licença / atribuição
Agregador de projetos open source; cada skill permanece sob a licença da sua origem. Veja `NOTICE.md`.
