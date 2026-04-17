# agent-skill-todoist-triage

An [Agent Skill](https://agentskills.io/) for triaging Todoist inbox tasks using a multi-dimensional system: MoSCoW priorities, time estimates, skill × leverage value tags, and context labels.

## What it does

Turns a flat Todoist inbox into a structured, actionable system by assigning four orthogonal dimensions to each task:

1. **Priority** (P1–P4) — MoSCoW: Must / Should / Could / Would
2. **Time estimate** (XS / S / M / L / XL) — T-shirt sizing
3. **Skill × Leverage** (`skill-low`/`skill-high` + `leverage-low`/`leverage-high`) — two clean orthogonal axes replacing the $10k Work dollar labels
4. **Context tags** — work type, status, energy, location, communication channel

Then places the task in the right project.

## Install

Copy the `todoist-triage/` directory into your agent's skills directory. For example, for VS Code / GitHub Copilot:

```
.agents/skills/todoist-triage/
```

For Claude Code, OpenCode, or other compatible agents, see their respective docs for skill installation paths.

## Usage

Once installed, ask your agent to triage your Todoist inbox, sort tasks, or prioritize items. The skill will activate automatically based on the description match.

Example prompts:
- "Triage my inbox"
- "Sort these tasks by priority and value"
- "Categorize these tasks with the right labels and project"

## Credits

Value framework inspired by [Khe Hy's $10k Work](https://coda.io/@khe-hy/10k-work).
