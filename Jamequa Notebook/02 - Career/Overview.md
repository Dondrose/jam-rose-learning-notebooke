---
type: overview
area: career
created: 2026-10-21
tags:
  - overview
  - career
---

# 💼 Career — Overview

> [!abstract] What this folder is for
> Everything about your working life and where you want it to go: your resume, the career fields you're exploring, job applications, skills you need, people to contact, and opportunities to follow up on.

## How to use this folder

- **`02-00-resume`** holds your resume itself — the current version, older versions, cover letters, and notes on what to change.
- **`02-01` to `02-03`** are one folder per **career field** you're exploring. Rename each placeholder to the actual field (e.g. `02-01-healthcare`, `02-02-design`) — keep the number at the front so the order stays the same. Add a fourth as `02-04-...` if needed.
- Inside a career-field folder, keep notes like: what the field is, job titles, required skills and certifications, companies, salary research, people you've talked to, and applications you've sent.
- **Don't put here:** course notes for skills you're learning (→ `03-training`) or articles and videos about the field (→ `04-research`). Link to them instead with `[[ ]]`.
- **Useful properties:** `status` (e.g. `idea`, `researching`, `applied`, `interview`, `closed`), `company`, `deadline`.

---

## 📊 All Career Notes

```base
filters:
  and:
    - file.inFolder("02-career")
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

## 📄 02-00 Resume

```base
filters:
  and:
    - file.inFolder("02-career/02-00-resume")
views:
  - type: table
    name: Resume files
    order:
      - file.name
      - file.ext
      - status
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 🧭 02-01 Career Field 1

```base
filters:
  and:
    - file.inFolder("02-career/02-01-career-field-1")
    - file.ext == "md"
views:
  - type: table
    name: Career field 1
    order:
      - file.name
      - status
      - company
      - deadline
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 🧭 02-02 Career Field 2

```base
filters:
  and:
    - file.inFolder("02-career/02-02-career-field-2")
    - file.ext == "md"
views:
  - type: table
    name: Career field 2
    order:
      - file.name
      - status
      - company
      - deadline
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

## 🧭 02-03 Career Field 3

```base
filters:
  and:
    - file.inFolder("02-career/02-03-career-field-3")
    - file.ext == "md"
views:
  - type: table
    name: Career field 3
    order:
      - file.name
      - status
      - company
      - deadline
      - file.mtime
    sort:
      - property: file.mtime
        direction: DESC
```

> [!note] Renaming a career-field folder
> If you rename `02-01-career-field-1`, Obsidian updates links automatically but **not** the folder path inside the base above. Edit the `file.inFolder("...")` line in that section to match the new name.

---

← [[Welcome]] · [[How To Use This Notebook]]
