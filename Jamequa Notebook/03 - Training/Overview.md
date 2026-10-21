---
type: overview
area: training
created: 2026-10-21
tags:
  - overview
  - training
---

# 🎓 Training — Overview

> [!abstract] What this folder is for
> Your hands-on learning: setting up your tools and working through skills step by step, starting with Python. These are **your own notes** from doing the work — what you installed, what you tried, what broke, and how you fixed it.

## How to use this folder

- **`03-01-setup`** — getting your computer and tools ready: installing Obsidian and its plugins, Python, a code editor, accounts you created, and any settings you changed. Write it so you could redo the setup on a new computer.
- **`03-02-python`** — Python lessons and practice: one note per lesson or topic (e.g. `Variables and Types`, `Loops`, `Exercise - Number Guessing Game`), with code snippets in ``` code blocks.
- **Adding a new subject:** create the next numbered folder, e.g. `03-03-sql` or `03-04-web-design`, and copy one of the sections below for it.
- **Don't put here:** the book, video or website you're learning *from* (→ `04-research`). Keep the source there and link to it, e.g. `Source: [[Python Crash Course]]`.
- **Useful properties:** `status` (`not-started`, `in-progress`, `done`), `lesson` (number), `source` (link to the research note).

---

## 📊 All Training Notes

```base
filters:
  and:
    - file.inFolder("03-training")
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
```

## 🛠️ 03-01 Setup

```base
filters:
  and:
    - file.inFolder("03-training/03-01-setup")
    - file.ext == "md"
views:
  - type: table
    name: Setup
    order:
      - file.name
      - status
      - tags
      - file.mtime
    sort:
      - property: file.name
        direction: ASC
```

## 🐍 03-02 Python

```base
filters:
  and:
    - file.inFolder("03-training/03-02-python")
    - file.ext == "md"
views:
  - type: table
    name: Python lessons
    order:
      - file.name
      - lesson
      - status
      - source
      - file.mtime
    sort:
      - property: lesson
        direction: ASC
  - type: table
    name: In progress
    filters:
      and:
        - status == "in-progress"
    order:
      - file.name
      - lesson
      - file.mtime
```

---

← [[Welcome]] · [[How To Use This Notebook]]
