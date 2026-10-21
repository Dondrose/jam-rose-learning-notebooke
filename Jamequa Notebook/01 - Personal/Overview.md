---
type: overview
area: personal
created: 2026-10-21
tags:
  - overview
  - personal
---

# 🌱 Personal — Overview

> [!abstract] What this folder is for
> Your life outside of work and study: goals, values, habits, health, relationships, journaling and reflection. If a note is about **you as a person** rather than your job, your learning, or a source you're reading, it belongs here.

## How to use this folder

- **Put here:** personal goals, habit trackers, journal entries, reflections, life plans, important dates, things you want to remember about yourself.
- **Don't put here:** job or resume material (→ `02-career`), course or tutorial notes (→ `03-training`), notes on books, videos or websites (→ `04-research`).
- **Name notes plainly**, e.g. `2026 Goals`, `Morning Routine`, `Reflection - 2026-10-21`.
- **Add properties** at the top of each note (`status`, `tags`) so they show up neatly in the table below.
- **Subfolders are optional for now.** When a topic grows past a handful of notes, create a numbered subfolder such as `01-01-goals` or `01-02-journal` and add a section for it on this page.

---

## 📊 All Personal Notes

```base
filters:
  and:
    - file.inFolder("01-personal")
    - file.ext == "md"
    - file.name != "Overview"
views:
  - type: table
    name: All notes
    order:
      - file.name
      - file.folder
      - status
      - tags
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
  - type: table
    name: Created this month
    filters:
      and:
        - file.ctime > now() - "30d"
    order:
      - file.name
      - tags
      - file.ctime
    sort:
      - property: file.ctime
        direction: DESC
```

---

← [[Welcome]] · [[How To Use This Notebook]]
