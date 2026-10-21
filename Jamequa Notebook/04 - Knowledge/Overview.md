---
type: overview
area: research
created: 2026-10-21
tags:
  - overview
  - research
---

# 🔬 Research — Overview

> [!abstract] What this folder is for
> Your library of **sources** — the books, videos, documents and websites you learn from — with your notes and takeaways for each one. Other folders link here when they use a source.

## How to use this folder

- **One note per source.** Name it after the source, e.g. `Atomic Habits`, `freeCodeCamp - Python for Beginners`.
- **`04-01-books`** — books and ebooks: author, what it's about, key ideas, favorite quotes, what you'll do differently.
- **`04-02-videos`** — YouTube videos, courses, talks: link, channel, length, timestamps of the useful parts.
- **`04-03-docs`** — PDFs, articles, manuals and handouts. You can drop the PDF itself in this folder next to its note.
- **`04-04-sites`** — websites and online tools worth coming back to: link, what it's good for, login hints (never passwords).
- **Useful properties:** `status` (`to-read`, `reading`, `done`), `author`, `url`, `rating` (1–5), and `area` (which pillar it supports: personal, career, training).

---

## 📊 All Research Notes

```base
filters:
  and:
    - file.inFolder("04-research")
    - file.name != "Overview"
views:
  - type: table
    name: All sources
    order:
      - file.name
      - file.folder
      - status
      - area
      - rating
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
  - type: table
    name: Reading list
    filters:
      and:
        - status == "to-read"
    order:
      - file.name
      - file.folder
      - area
```

## 📚 04-01 Books

```base
filters:
  and:
    - file.inFolder("04-research/04-01-books")
    - file.ext == "md"
views:
  - type: table
    name: Books
    order:
      - file.name
      - author
      - status
      - rating
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 🎬 04-02 Videos

```base
filters:
  and:
    - file.inFolder("04-research/04-02-videos")
    - file.ext == "md"
views:
  - type: table
    name: Videos
    order:
      - file.name
      - author
      - url
      - status
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 📑 04-03 Docs

```base
filters:
  and:
    - file.inFolder("04-research/04-03-docs")
views:
  - type: table
    name: Documents
    order:
      - file.name
      - file.ext
      - author
      - status
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 🌐 04-04 Sites

```base
filters:
  and:
    - file.inFolder("04-research/04-04-sites")
    - file.ext == "md"
views:
  - type: table
    name: Sites
    order:
      - file.name
      - url
      - area
      - tags
      - file.mtime
    sort:
      - property: file.name
        direction: ASC
```

---

← [[Welcome]] · [[How To Use This Notebook]]
