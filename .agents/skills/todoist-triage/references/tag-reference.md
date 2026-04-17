# Tag Reference

Complete reference for all tag dimensions used in the triage system.

## Priority (MoSCoW)

The priority field is set via Todoist's native `priority` field, not labels.

| Prio | Meaning | When to use | Todoist field |
|------|---------|-------------|---------------|
| P1 | **Must** | Deadlines, commitments, urgent blockers | `priority: "p1"` |
| P2 | **Should** | Important but not time-critical, this week | `priority: "p2"` |
| P3 | **Could** | Would be nice, no commitment | `priority: "p3"` |
| P4 | **Would** | Someday/maybe, parking lot | `priority: "p4"` (default) |

**Defaults:** If unsure, assign P3. Only P1/P2 should feel like commitments.

## Time Estimates (T-Shirt Labels)

| Label | Effort | Guideline |
|-------|--------|-----------|
| `XS` | Few minutes | Quick reply, quick lookup, one click |
| `S` | ~30 min | 1 Pomodoro. Single focused task. |
| `M` | ~1 hour | Needs a substantial time block. Multiple steps. |
| `L` | Several hours | Half a day. Complex task with substeps. |
| `XL` | ~1 day | It's a project. Break into subtasks. |

**Rule of thumb:** If you can't describe the "done" state in one sentence, it's probably M or larger.

## Impact × Leverage Tags

Two orthogonal label axes inspired by Khe Hy's [$10k Work](https://coda.io/@khe-hy/10k-work) framework:

### The Two Labels

| Label | Meaning |
|-------|---------|
| `impact-low` | Low specialization — anyone could do this |
| `impact-high` | High specialization — requires your expertise |
| `leverage-low` | Affects one case, one person |
| `leverage-high` | Affects many people or whole systems |

### The 2×2 Matrix

```
              leverage-low    leverage-high
             ┌────────────────┬────────────────┐
impact-high  │  Specialized   │  Strategic     │
             │  individual    │  systemic      │
             ├────────────────┼────────────────┤
impact-low   │  Manual        │  Systemic      │
             │  direct        │  automated     │
             └────────────────┴────────────────┘
```

### impact-low + leverage-low — Manual Labor
- One-off, hands-on, no scaling
- Examples: Answering an email, data entry, booking a flight

### impact-low + leverage-high — Busywork at Scale
- Systemic, reusable, automates or standardizes
- Examples: Script that helps 20 people, docs that save 50 questions, automatic reminder, template

### impact-high + leverage-low — Expert Work
- Difficult, individual — only you can do it
- Examples: Hard bug, architecture decision, incident management, 1:1 coaching

### impact-high + leverage-high — Strategic Systemic
- Changes whole systems, strategic + systemic
- Examples: Platform architecture, product vision, process redesign, hiring framework

### Decision Guide

Ask two questions:
1. **"Does this require specialized skill only I have?"** → Yes = `impact-high`
2. **"Does this affect many people/systems?"** → Yes = `leverage-high`

If both are yes → protect this work with deep-focus blocks.

## Context Tags

### Work Type
| Tag | Meaning |
|-----|---------|
| `reading` | Reading task (article, docs, book) |
| `deep-focus` | Needs concentrated, uninterrupted time |

### Status
| Tag | Meaning |
|-----|---------|
| `waiting` | Blocked on someone/something. **Must** add comment with reason + reschedule date. |
| `next` | The single next physical action (GTD). Not "plan X" but "draft email to Y about X". |

### Energy
| Tag | Meaning |
|-----|---------|
| `energy-low` | Can be done when tired. Low cognitive load. |

### Location
| Tag | Meaning |
|-----|---------|
| `home` | Do at home |
| `errands` | Do while out and about |

### Communication
| Tag | Meaning |
|-----|---------|
| `call` | Phone/video call needed |
| `email` | Handle via email |
| `messenger` | Signal, WhatsApp, etc. |

## Tag Combinations

Common effective combinations:

| Pattern | Tags | Example |
|---------|------|---------|
| Quick win | `XS impact-low leverage-high next` | "Write script to automate daily report" |
| Deep work block | `L impact-high leverage-high deep-focus` | "Design new API architecture" |
| Low energy task | `XS impact-low leverage-low energy-low` | "Reply to non-urgent emails" |
| Blocked item | `M impact-high leverage-low waiting` | "Review PR — waiting on author response" |
| Errand | `S impact-low leverage-low errands` | "Pick up package from post office" |
