# Obsidian Starter Vault Template

A portable, opinionated vault seed using **PARA** (Projects / Areas / Resources / Archive)
combined with **LYT Maps of Content**. Open this folder in Obsidian — plugins and theme
load automatically, no manual setup required.

---

## Table of contents

1. [First-time setup](#1-first-time-setup)
2. [Folder structure](#2-folder-structure)
3. [Daily workflow](#3-daily-workflow)
4. [Keyboard shortcuts — Obsidian core](#4-keyboard-shortcuts--obsidian-core)
5. [Keyboard shortcuts — Community plugins](#5-keyboard-shortcuts--community-plugins)
6. [Templates reference](#6-templates-reference)
7. [PARA in practice](#7-para-in-practice)
8. [Task syntax (Tasks plugin)](#8-task-syntax-tasks-plugin)
9. [Dataview cheat-sheet](#9-dataview-cheat-sheet)
10. [Git backup](#10-git-backup)
11. [Customising the vault](#11-customising-the-vault)
12. [Plugins & themes reference](#12-plugins--themes-reference)
13. [Troubleshooting](#13-troubleshooting)

---

## 1. First-time setup

```
Obsidian → Open folder as vault → select this directory
```

When prompted: **Trust & Enable** community plugins. The theme (VSCode Dark Modern)
and all plugins load from the bundled `.obsidian/` folder — nothing is downloaded.

**Verify everything is working:**

| Check | Where to look |
|-------|---------------|
| Theme applied (dark, VS Code style) | Settings → Appearance |
| 11 plugins enabled | Settings → Community plugins |
| Today's daily note works | `Cmd/Ctrl+P` → *Open today's daily note* |

---

## 2. Folder structure

```
obsidian-template/
├── 00_Inbox/           ← capture everything here first
│   ├── Daily/          ← daily notes (auto-created by Periodic Notes)
│   └── Weekly/         ← weekly reviews
├── 01_Projects/        ← finite work with a clear outcome
├── 02_Areas/           ← ongoing responsibilities (no end date)
├── 03_Resources/       ← reference, research, playbooks
│   └── Playbooks/
├── 04_Archive/         ← completed / inactive items
├── 05_MOCs/            ← Maps of Content (topic entry points)
├── 90_Meta/
│   └── Templates/      ← Templater templates — do not move or rename
├── 90_Personal/        ← private notes, excluded from git
├── Home.md             ← vault dashboard (start here)
└── README.md           ← this file
```

**Decision rule for where to put a note:**

1. Am I actively working toward an outcome? → `01_Projects/`
2. Is it an ongoing responsibility? → `02_Areas/`
3. Is it reference material I might use later? → `03_Resources/`
4. Not sure yet? → `00_Inbox/` and triage later

---

## 3. Daily workflow

### Morning (2 min)

1. `Cmd/Ctrl+Shift+D` — open today's daily note (or Command Palette → *Open today's daily note*)
2. Write today's intention at the top
3. Review the auto-populated Tasks query for anything due today

### During the day

- Capture a fleeting thought → create a note in `00_Inbox/` (Capture template auto-applies)
- Link to relevant notes with `[[double brackets]]`
- Add tasks with `- [ ] task text` anywhere in a note

### End of day / week

- Check off completed tasks: click the checkbox or press `Alt+Enter` on a task line
- Friday: `Cmd/Ctrl+P` → *Open this week's weekly note* for a weekly review

---

## 4. Keyboard shortcuts — Obsidian core

> **Mac** uses `Cmd`; **Windows / Linux** uses `Ctrl`. `Opt` = `Alt` on Windows.

### Navigation

| Shortcut | Action |
|----------|--------|
| `Cmd+O` | Quick switcher — open any note by name |
| `Cmd+Shift+F` | Search across all files |
| `Cmd+P` | Command palette — run any command |
| `Cmd+Alt+←` | Navigate back |
| `Cmd+Alt+→` | Navigate forward |
| `Cmd+Click` on link | Open link in new tab |
| `Cmd+Shift+Click` | Open link in new pane (split) |
| `Alt+Enter` | Follow link under cursor |

### Editing

| Shortcut | Action |
|----------|--------|
| `Cmd+N` | New note |
| `Cmd+B` | **Bold** |
| `Cmd+I` | *Italic* |
| `Cmd+K` | Insert markdown link |
| `Cmd+]` | Indent list item |
| `Cmd+[` | Unindent list item |
| `Cmd+Enter` | Toggle checklist item done |
| `Cmd+D` | Delete current line |
| `Cmd+Z` / `Cmd+Shift+Z` | Undo / Redo |

### View & panels

| Shortcut | Action |
|----------|--------|
| `Cmd+E` | Toggle reading / editing mode |
| `Cmd+\` | Toggle left sidebar |
| `Cmd+Shift+\` | Toggle right sidebar |
| `Cmd+,` | Open settings |
| `Cmd+W` | Close current tab |
| `Cmd+Shift+T` | Reopen last closed tab |
| `Cmd+G` | Open graph view |
| `Cmd+Shift+G` | Open local graph for current note |

### Headings (in edit mode)

| Shortcut | Action |
|----------|--------|
| `Cmd+1` … `Cmd+6` | Set heading level H1–H6 |
| `Cmd+0` | Remove heading (plain paragraph) |

---

## 5. Keyboard shortcuts — Community plugins

### Templater

| Shortcut | Action |
|----------|--------|
| `Alt+E` | Insert a template at cursor |
| `Alt+N` | Create new note from template (pick template + filename) |
| *(auto)* | When you create a file in `00_Inbox/`, `01_Projects/`, or `03_Resources/`, the matching template is applied automatically |

> **Folder auto-template mapping:**
> | Folder | Template applied |
> |--------|-----------------|
> | `00_Inbox/` | `Capture.md` |
> | `01_Projects/` | `Project-RFC.md` |
> | `03_Resources/` | `Learning.md` |

### Periodic Notes

| Shortcut / Command | Action |
|--------------------|--------|
| `Cmd+P` → *Open today's daily note* | Create or open today's note in `00_Inbox/Daily/` |
| `Cmd+P` → *Open this week's weekly note* | Create or open this week's review in `00_Inbox/Weekly/` |

> **Tip:** Set a hotkey for these two commands in Settings → Hotkeys → search "periodic".
> Recommended: `Cmd+Shift+D` for daily, `Cmd+Shift+W` for weekly.

### Omnisearch (full-text search)

| Shortcut | Action |
|----------|--------|
| `Cmd+Shift+O` | Open Omnisearch modal — searches note titles AND body text |

### Tasks plugin

| Shortcut | Action |
|----------|--------|
| `Cmd+P` → *Tasks: Create or edit task* | Open task-editing modal on current line |
| Click checkbox | Toggle task done (also stamps completion date) |
| `Cmd+Enter` (on a `- [ ]` line) | Toggle done inline |

### Obsidian Git

| Shortcut / Command | Action |
|--------------------|--------|
| `Cmd+P` → *Git: Commit all changes* | Commit everything with an auto-message |
| `Cmd+P` → *Git: Push* | Push to remote (after you add one) |
| `Cmd+P` → *Git: Pull* | Pull from remote |

> **Auto-backup:** Enable in Settings → Obsidian Git → *Auto backup every X minutes*.

### Excalidraw

| Shortcut | Action |
|----------|--------|
| `Cmd+P` → *Excalidraw: Create new drawing* | New whiteboard canvas |
| `Ctrl+1` / `Ctrl+2` … | Switch tools inside Excalidraw (select, rectangle, text…) |
| `Ctrl+Shift+E` (inside drawing) | Export to PNG / SVG |

### Advanced URI

Lets you create deep-links to any note or heading. Useful for linking from
external apps (Notion, calendar apps, shortcuts).

```
obsidian://advanced-uri?vault=obsidian-template&filepath=Home.md
```

`Cmd+P` → *Advanced URI: Copy URI for current file*

---

## 6. Templates reference

All templates live in `90_Meta/Templates/`. Every template injects today's date
via `<% tp.date.now("YYYY-MM-DD") %>` and writes standard YAML frontmatter.

| Template | Type field | Best used in | Key sections |
|----------|------------|--------------|--------------|
| `Capture.md` | `capture` | `00_Inbox/` | Idea, Context, Next action |
| `Project-RFC.md` | `rfc` | `01_Projects/` | Problem, Goals, Approach, Tasks |
| `Learning.md` | `resource` | `03_Resources/` | Summary, Key concepts, Connections |
| `Daily-Note.md` | `capture` | `00_Inbox/Daily/` | Intention, Tasks query, Wins, Blockers |
| `Weekly-Review.md` | `capture` | `00_Inbox/Weekly/` | Completed tasks (auto), Open loops, Intentions |
| `Meeting.md` | `meeting` | anywhere | Agenda, Discussion, Decisions, Action items |
| `Decision.md` | `decision` | `02_Areas/` | Context, Decision, Rationale, Consequences |
| `Runbook.md` | `runbook` | `03_Resources/` | Prerequisites, Steps, Verification, Rollback |
| `MOC.md` | `moc` | `05_MOCs/` | Core concepts, Dataview project/resource tables |

### YAML frontmatter schema

```yaml
---
type: capture | rfc | resource | meeting | decision | runbook | moc
status: draft | active | parked | done | obsolete
area: <slug>          # e.g. "engineering", "health", "finance"
project: <slug>       # leave empty if this is an Area/Resource note
tags: []
created: YYYY-MM-DD   # auto-filled by Templater
updated: YYYY-MM-DD   # auto-bumped on save by Linter
---
```

---

## 7. PARA in practice

### Projects vs Areas — the key distinction

> A **Project** has a finish line. An **Area** does not.

| Example | Classification |
|---------|----------------|
| "Launch v2.0 of the API" | Project (`01_Projects/`) |
| "Engineering" | Area (`02_Areas/`) |
| "Run a marathon" | Project |
| "Health & Fitness" | Area |
| "Write the ADR for auth redesign" | Project |
| "Architecture decisions" | Area |

### Triage flow for inbox notes

```
00_Inbox/ note
    │
    ├─ Is it actionable?
    │       ├─ Yes, finite → move to 01_Projects/ (or link from project note)
    │       └─ Yes, ongoing → move to 02_Areas/
    │
    ├─ Is it reference material?
    │       └─ Yes → move to 03_Resources/
    │
    └─ No longer relevant → delete or 04_Archive/
```

### MOC pattern

Create a new MOC whenever a topic has more than ~5 notes:

1. `Cmd+P` → *Templater: Create new note from template* → choose `MOC.md`
2. Save to `05_MOCs/<topic-name>.md`
3. Set `area:` in frontmatter to match your Area note's slug
4. Link the MOC from `05_MOCs/000-Index.md` and from `Home.md`

---

## 8. Task syntax (Tasks plugin)

```markdown
- [ ] Basic task
- [ ] Task with due date 📅 2026-06-01
- [ ] Task with scheduled date ⏳ 2026-05-20
- [ ] High priority ⏫
- [ ] Medium priority 🔼
- [ ] Low priority 🔽
- [x] Completed task ✅ 2026-05-18
- [-] Cancelled task
```

### Query tasks in any note

````markdown
```tasks
not done
due before 2026-06-01
path includes 01_Projects
```
````

### Useful query filters

| Filter | Meaning |
|--------|---------|
| `not done` | All open tasks |
| `due today` | Due on today's date |
| `due before next week` | Overdue + this week |
| `path includes 01_Projects` | Only tasks in Projects folder |
| `has tag #area/health` | Tasks tagged with a specific tag |
| `priority is high` | High-priority tasks only |

---

## 9. Dataview cheat-sheet

### List all active projects

````markdown
```dataview
TABLE status, area FROM "01_Projects"
WHERE status = "active"
SORT file.mtime DESC
```
````

### List all notes in an area

````markdown
```dataview
LIST FROM "02_Areas"
WHERE area = "engineering"
SORT file.name ASC
```
````

### Show recently modified notes

````markdown
```dataview
TABLE file.mtime AS "Modified" FROM ""
SORT file.mtime DESC
LIMIT 15
```
````

### Inline field query

Add `key:: value` anywhere in a note body (not just YAML) and Dataview picks it up:

```markdown
progress:: 60%
owner:: alice
```

---

## 10. Git backup

The vault is a local git repo. No remote is configured by default.

### Add a remote (optional)

```bash
cd /path/to/obsidian-template
git remote add origin https://github.com/you/your-vault.git
git push -u origin main
```

### Manual backup via Obsidian Git plugin

- `Cmd+P` → *Git: Commit all changes* → auto-generates a commit message
- `Cmd+P` → *Git: Push*

### Auto-backup

Settings → Community plugins → Obsidian Git → **Auto backup interval** (e.g. 10 min)

### What is and isn't committed

| Committed | Not committed |
|-----------|---------------|
| All markdown notes | `workspace.json` (per-machine state) |
| Plugin JS + manifests | `graph.json` |
| Theme CSS | `.DS_Store` |
| Templates | `90_Personal/**` (private) |
| Config JSON files | `cache/` |

---

## 11. Customising the vault

### Change the default theme

Settings → Appearance → Themes → pick from:
- VSCode Dark Modern (default)
- Minimal
- AnuPpuccin
- Things

### Add a hotkey for daily / weekly note

Settings → Hotkeys → search **"periodic"** → assign `Cmd+Shift+D` / `Cmd+Shift+W`

### Add a new folder template mapping (Templater)

Settings → Templater → *Folder Templates* → add a row:

| Folder | Template |
|--------|----------|
| `02_Areas/` | `90_Meta/Templates/MOC.md` |

### Swap or add a plugin

Settings → Community plugins → Browse → install → reload vault.
Then commit the new plugin folder:

```bash
git add .obsidian/plugins/<new-plugin-id>/
git commit -m "feat: add <plugin-name>"
```

---

## 12. Plugins & themes reference

### Plugins

| Plugin | Settings location | Key config |
|--------|------------------|------------|
| **Dataview** | Settings → Dataview | DataviewJS enabled, inline fields on |
| **Templater** | Settings → Templater | Template folder: `90_Meta/Templates/`, folder auto-templates on |
| **Periodic Notes** | Settings → Periodic Notes | Daily: `00_Inbox/Daily/`, Weekly: `00_Inbox/Weekly/` |
| **Tasks** | Settings → Tasks | Done date stamped automatically |
| **Linter** | Settings → Linter | Runs on save; bumps `updated:` field; ignores `90_Personal/` |
| **Omnisearch** | No config needed | Full-text fuzzy search |
| **Obsidian Git** | Settings → Obsidian Git | Set auto-backup interval |
| **Excalidraw** | Settings → Excalidraw | Drawings stored as `.excalidraw.md` |
| **Advanced URI** | No config needed | Copy URI from Command Palette |
| **URL Into Selection** | No config needed | Select text, paste URL → auto-formats as `[text](url)` |
| **Mermaid Tools** | No config needed | Adds toolbar for mermaid diagram types |

### Themes

| Theme | Style |
|-------|-------|
| **VSCode Dark Modern** | Dark, monospace-influenced, familiar to devs |
| **Minimal** | Clean, neutral, highly customisable via Style Settings |
| **AnuPpuccin** | Pastel Catppuccin palette, colourful |
| **Things** | macOS Things-app aesthetic, warm tones |

---

## 13. Troubleshooting

| Problem | Fix |
|---------|-----|
| Plugin shows "failed to load" | Settings → Community plugins → find plugin → *Reload* |
| Templater doesn't auto-apply | Settings → Templater → confirm "Trigger on new file creation" is ON |
| Daily note goes to wrong folder | Settings → Periodic Notes → set Daily folder to `00_Inbox/Daily/` |
| Linter overwrites my dates | Settings → Linter → YAML Timestamp → adjust `created`/`updated` key names |
| Dataview shows nothing | Confirm frontmatter field names match the query (`FROM "01_Projects"`, `WHERE status = "active"`) |
| Theme not applied | Settings → Appearance → CSS Theme → select *VSCode Dark Modern* |
| Git commit fails | Ensure you're inside the vault folder: `git -C /path/to/vault status` |

---

## Build info

- Built: 2026-05-18
- Framework: PARA + LYT MOCs
- Git: local only (`vault@local`) — add your own remote to sync
- Prompt playbook: `03_Resources/Playbooks/Generate-Vault-Template-Prompt.md`
