# The Agent Development Kit

Five layers, one stack. Source mark: GenAI.works.

Use this file when the work is deciding where a rule, a skill, a hook, a subagent, or a shared plugin belongs. Open it from `C:\Users\ANISH\Documents\ai-playbook\LIBRARY.md` and open only the layer the work needs.

Folder root: `agent-dev-kit/`

Flow: CLAUDE.md sets rules, Skills provide expertise, Hooks enforce quality, Subagents delegate work, Plugins distribute to the team.

## Layer 1. CLAUDE.md, the memory layer

- `architecture.rules` — naming, structure, and repo expectations
- `global.md` — lives at `~/.claude/` for every project
- `project.md` — lives at `.claude/` for this repo only

## Layer 2. Skills, the knowledge layer

Folder: `skills/`

- `SKILL.md` — description matched and auto invoked
- `scripts/` — reference scripts and templates
- `context.md` — on demand, isolated subagent

## Layer 3. Hooks, the guardrail layer

Folder: `hooks/`

- `PreToolUse.sh` — block `rm -rf` and validate before run
- `PostToolUse.sh` — auto lint on write and ping Slack
- `SessionStart.sh` — deterministic, not AI

Caption: hooks block `rm -rf`, auto-lint on write, and ping Slack on session start. They do not guess.

Labels on the poster, not a second system: MCP Server, external tools, GitHub, database, APIs, custom, and Agent Teams (parallel execution, message passing, lead, shared permissions).

## Layer 4. Subagents, the delegation layer

Folder: `subagents/`

- `code-reviewer.md`
- `test-runner.md`
- `explorer.md`

Each gets its own context window, custom tools, and custom permissions, and returns only results, so the main context stays clean.

## Layer 5. Plugins, the distribution layer

Folder: `plugins/`

- `manifest.json` — bundles skills, agents, hooks, and commands
- `marketplace.url` — npm packages for agent capabilities
- `team.install` — one install and every teammate is on the same skills, hooks, and commands
