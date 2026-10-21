---
type: guide
created: 2026-10-21
tags:
  - guide
  - index
---

# 📘 How To Use This Notebook

> [!abstract] Start here
> This page explains three things: **how to use Obsidian** (the app), **how this notebook is organized**, and **what's coming next** in plugins and customization. Keep it open in a tab until it feels natural.

**Contents**
1. [[#1. Using Obsidian]]
2. [[#2. How this notebook is structured]]
3. [[#3. Plugins and customization (coming soon)]]

---

## 1. Using Obsidian

Obsidian is a note-taking app that works on plain text files saved on your computer. Every note is a `.md` (Markdown) file inside this notebook's folder — nothing is locked inside the app, and you can open the files with any text editor.

### Getting around

| Action | How |
|---|---|
| Open any note fast | `Ctrl/Cmd + O` (Quick Switcher), then type part of its name |
| Run any command | `Ctrl/Cmd + P` (Command Palette) |
| Search every note | `Ctrl/Cmd + Shift + F` |
| Create a new note | `Ctrl/Cmd + N`, or right-click a folder → **New note** |
| Toggle reading vs. editing | `Ctrl/Cmd + E` |
| Go back / forward | `Ctrl/Cmd + Alt + ←` / `→` |
| See the folder list | Left sidebar → **Files** icon |
| See what links to this note | Right sidebar → **Backlinks** |
| See an outline of headings | Right sidebar → **Outline** |

> [!tip] Hover to preview
> Hold `Ctrl/Cmd` and hover over any link to preview the note without leaving the page.

### Writing notes (Markdown basics)

| You type | You get |
|---|---|
| `# Heading`, `## Smaller heading` | Headings |
| `**bold**`, `*italic*`, `==highlight==` | **bold**, *italic*, ==highlight== |
| `- item` | Bullet list |
| `1. item` | Numbered list |
| `- [ ] task` | Checkbox you can tick |
| `` `code` `` and ```` ``` ```` blocks | Code (great for Python notes) |
| `> quote` | Quote |
| `---` | Divider line |

### Linking notes together

Links are what make Obsidian powerful — link ideas instead of only filing them.

- **Link to a note:** type `[[` and start typing a note name. If the note doesn't exist yet, clicking the link creates it.
- **Show different text:** `[[Atomic Habits|that habits book]]`.
- **Link to a heading:** `[[How To Use This Notebook#1. Using Obsidian]]`.
- **Embed a note or image inside another note:** add `!` in front — `![[My Resume]]`, `![[photo.png]]`.
- **Drag & drop** images or PDFs into a note to attach them.

### Properties (the box at the top of a note)

Properties are small labelled fields at the top of a note. They power the tables on each Overview page.

```yaml
---
status: in-progress
tags:
  - python
source: "[[Python Crash Course]]"
---
```

- Add them with `Ctrl/Cmd + ;` or the command **Add file property**.
- Common ones used in this notebook: `status`, `tags`, `area`, `source`, `author`, `url`, `rating`, `deadline`. Each folder's Overview lists the ones that are useful there.

### Tags

Add `#tag` anywhere in a note, or under `tags` in properties. Click a tag to see every note with it. Use tags for **themes that cut across folders** (e.g. `#goal`, `#idea`, `#follow-up`); use folders for **where a note lives**.

### Callouts

Coloured boxes for emphasis:

```markdown
> [!tip] Title
> Your text here.
```

Types you'll use: `note`, `tip`, `important`, `warning`, `question`, `todo`, `quote`, `abstract`.

### Bases (the live tables)

Each Overview page contains **Bases** — live tables that automatically list every note in a folder. You don't edit the tables; you just add notes to the folder and fill in properties, and they appear.

- Click a column header to sort.
- Use the view menu at the top-left of a table to switch views (some tables have more than one, e.g. *Reading list*).
- Bases require Obsidian **1.9 or newer** (*Settings → About* to check).

### Other built-in tools that are switched on

- **Daily notes** — the calendar icon in the left ribbon creates today's note for quick capture.
- **Templates** — insert reusable note layouts (see section 3).
- **Graph view** — `Ctrl/Cmd + G` shows how notes link to each other.
- **Canvas** — a whiteboard for arranging notes and ideas visually.
- **Bookmarks** — star notes you open often.
- **File recovery** — *Settings → File recovery* restores earlier versions of a note if something goes wrong.
- **Sync** — keeps the notebook in step across devices.

---

## 2. How this notebook is structured

### The folders

```
Jamequa Notebook/
├── Welcome.md                    ← home page
├── How To Use This Notebook.md   ← this page
├── 01-personal/                  ← life, goals, habits, reflection
│   └── Overview.md
├── 02-career/                    ← resume and career fields
│   ├── Overview.md
│   ├── 02-00-resume/
│   ├── 02-01-career-field-1/
│   ├── 02-02-career-field-2/
│   └── 02-03-career-field-3/
├── 03-training/                  ← hands-on learning
│   ├── Overview.md
│   ├── 03-01-setup/
│   └── 03-02-python/
└── 04-research/                  ← sources: books, videos, docs, sites
    ├── Overview.md
    ├── 04-01-books/
    ├── 04-02-videos/
    ├── 04-03-docs/
    └── 04-04-sites/
```

| Folder | Use it for | Overview |
|---|---|---|
| 🌱 `01-personal` | Goals, values, habits, journaling, life planning | [[01-personal/Overview\|Personal Overview]] |
| 💼 `02-career` | Resume, career fields being explored, applications, contacts | [[02-career/Overview\|Career Overview]] |
| 🎓 `03-training` | Tool setup and step-by-step skill learning (starting with Python) | [[03-training/Overview\|Training Overview]] |
| 🔬 `04-research` | One note per source you learn from | [[04-research/Overview\|Research Overview]] |

### The rules

1. **Numbers keep the order.** Top-level folders are `01`–`04`; subfolders take their parent's number plus their own (`02-01`, `02-02`…). New folders get the next number, e.g. `03-03-sql`.
2. **Lowercase-with-dashes for folders** (`04-02-videos`); **normal readable names for notes** (`Python Loops`, `2026 Goals`).
3. **Every top-level folder has one `Overview.md`.** It explains what goes in the folder and shows a live table for each subfolder. When you add a subfolder, copy one of the base sections on that Overview and change the folder path in `file.inFolder("...")`.
4. **A note lives in one folder but can link to many.** Python lesson notes live in `03-training`; the book they come from lives in `04-research`; link between them.
5. **Not sure where something goes?** Create it in the notebook root for now and move it later — capture first, organize later. Dragging a note to a new folder keeps all its links working.
6. **Fill in `status`** on notes you're actively working on so the Overview tables stay useful.

### Where does it go? (quick guide)

| If it's… | Put it in |
|---|---|
| A goal, habit, or journal entry | `01-personal` |
| Your resume or a cover letter | `02-career/02-00-resume` |
| Research on a job, company, or career path | the matching `02-career/02-0x-...` field folder |
| Notes on installing or configuring something | `03-training/03-01-setup` |
| A Python lesson or exercise | `03-training/03-02-python` |
| Notes on a book, video, article, or website | the matching `04-research/04-0x-...` folder |

---

## 3. Plugins and customization (coming soon)

> [!todo] Placeholder section
> These plugins are already installed. Setup instructions and how-to guides for each will be added here as they're configured. Until then, it's safe to leave them alone.

### Community plugins (installed)

| Plugin | What it will be used for | Status |
|---|---|---|
| **Templater** | Ready-made templates for new notes in each folder (lesson, book, career field, journal) | ⏳ To be configured |
| **Tasks** | Tracking to-dos with due dates across the whole notebook | ⏳ To be configured |
| **Calendar** | Sidebar calendar for opening daily notes | ⏳ To be configured |
| **Obsidian Git** | Automatic backups / version history of the notebook | ⏳ To be configured |
| **Advanced Tables** (table-editor) | Easier editing and formatting of Markdown tables | ⏳ To be configured |
| **Mermaid Tools** | Drawing simple diagrams and flowcharts inside notes | ⏳ To be configured |
| **Style Settings** | Adjusting colours, fonts, and theme options | ⏳ To be configured |

### Templater
> [!todo] Instructions coming soon
> - Templates folder location: _TBD_
> - Template list (one per folder type): _TBD_
> - How to insert a template / hotkey: _TBD_

### Tasks
> [!todo] Instructions coming soon
> - Task format and due dates: _TBD_
> - Where task lists will appear (dashboards): _TBD_

### Calendar & Daily Notes
> [!todo] Instructions coming soon
> - Daily notes folder and naming: _TBD_
> - Daily note template: _TBD_

### Obsidian Git (backup)
> [!todo] Instructions coming soon
> - Backup schedule: _TBD_
> - How to restore an older version: _TBD_

### Advanced Tables
> [!todo] Instructions coming soon
> - Table shortcuts: _TBD_

### Mermaid Tools
> [!todo] Instructions coming soon
> - Example diagrams: _TBD_

### Style Settings & appearance
> [!todo] Instructions coming soon
> - Theme: _TBD_
> - CSS snippets: _TBD_
> - Colour/font choices: _TBD_

### Other customization
> [!todo] Planned
> - Custom hotkeys: _TBD_
> - Bookmarked notes / workspace layout: _TBD_
> - Area dashboards and review notes (daily, weekly, monthly): _TBD_
> - Additional plugins: _TBD_

---

← [[Welcome]]

*Last updated: 2026-10-21*
