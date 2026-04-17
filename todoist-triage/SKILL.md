---
name: todoist-triage
description: Triage and manage Todoist inbox tasks using a multi-dimensional system (MoSCoW priorities, time estimates, $10k-work value tags, and context labels). Use when sorting, triaging, prioritizing, or organizing tasks in Todoist, or when the user mentions inbox cleanup, task categorization, or task dimensions.
metadata:
  author: crn
  version: "1.0"
---

# Todoist Triage

Triage incoming tasks by assigning four orthogonal dimensions before placing them in the right project. This skill turns a flat inbox into a structured, actionable system.

## CRITICAL RULE

**NEVER delete any Todoist object without explicit user confirmation.** Before calling any delete tool:

1. STOP and show exactly what will be deleted (type, name/content, ID)
2. Wait for explicit "yes", "ja", "ok" or similar confirmation
3. Only proceed after confirmation

No exceptions — even if the user said "delete" in a general context.

## Triage Workflow

When triaging a task, apply these dimensions **in order**:

### 1. Priority (MoSCoW)

Assign one priority level:

| Prio | Meaning | Todoist Field |
|------|---------|---------------|
| P1 | **Must** — has to be done | `priority: "p1"` |
| P2 | **Should** — should be done | `priority: "p2"` |
| P3 | **Could** — nice to have | `priority: "p3"` |
| P4 | **Would** — someday/maybe | `priority: "p4"` (default) |

### 2. Time Estimate (T-Shirt Size)

Add one time label:

| Label | Effort |
|-------|--------|
| `XS` | Few minutes ("snack size") |
| `S` | ~30 min (1 Pomodoro) |
| `M` | ~1 hour (substantial block) |
| `L` | Several hours |
| `XL` | ~1 day (it's a project) |

### 3. Impact × Leverage (2D Value Tags)

Add **two** labels — one for each axis:

| Label | Axis | Meaning |
|-------|------|---------|
| `impact-low` | Impact | Low specialization, anyone could do it |
| `impact-high` | Impact | High specialization, requires your expertise |
| `leverage-low` | Leverage | Affects one case, one person |
| `leverage-high` | Leverage | Affects many people or whole systems |

The combination tells you what kind of work it is:

| Combination | Character | Examples |
|-------------|-----------|---------|
| `impact-low` + `leverage-low` | Manual, direct | Answering emails, data entry |
| `impact-low` + `leverage-high` | Systemic, automated — "busywork at scale" | Script helping 20 people, docs saving 50 questions |
| `impact-high` + `leverage-low` | Specialized, individual — expertise without scale | Hard bug, architecture decision, incident mgmt |
| `impact-high` + `leverage-high` | Strategic + systemic — changes whole systems | Platform architecture, product vision, process design |

**Key:** Impact and leverage are orthogonal. High leverage doesn't mean high impact, and vice versa.

### 4. Context Tags

Add relevant context labels:

| Category | Tags |
|----------|------|
| **Work type** | `reading`, `deep-focus` |
| **Status** | `waiting`, `next` |
| **Energy** | `energy-low` |
| **Location** | `home`, `errands` |
| **Communication** | `call`, `email`, `messenger` |

### 5. Assign to Project

Place the task in the correct project. Read [project structure reference](references/project-structure.md) for the full project list and important sections.

## Gotchas

- Tasks with `waiting` status MUST include a comment explaining what they're blocked on and a reschedule date
- `next` tag = the single next physical action (GTD-style) — not "plan the project" but "draft the email"
- `impact-high` + `leverage-high` work should be protected — schedule deep-focus blocks, don't let it get squeezed by `impact-low` + `leverage-low` tasks
- An `XL` task is actually a project — consider breaking it into subtasks
- Tasks without a time estimate are invisible to planning — always assign one

## Triage Checklist

For each inbox task:

- [ ] Priority assigned (P1–P4)
- [ ] Time estimate label added (XS–XL)
- [ ] Impact label added (impact-low or impact-high)
- [ ] Leverage label added (leverage-low or leverage-high)
- [ ] Context tags added (at least one if applicable)
- [ ] Project assigned
- [ ] `next` tag added if this is the immediate next action
- [ ] `waiting` tag + comment + reschedule date if blocked
