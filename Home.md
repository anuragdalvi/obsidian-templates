---
type: moc
status: active
area: home
tags: [moc, home]
created: 2026-05-18
updated: 2026-05-18
---

# Home

_The single entry point for this vault. Navigate everything from here._

## PARA Index

| Folder | Purpose |
|--------|---------|
| [[00_Inbox/]] | Unprocessed captures, daily + weekly notes |
| [[01_Projects/]] | Finite work with a clear outcome |
| [[02_Areas/]] | Ongoing responsibilities with a standard to maintain |
| [[03_Resources/]] | Reference material, research, playbooks |
| [[04_Archive/]] | Completed or inactive PARA items |
| [[05_MOCs/000-Index\|MOC Index]] | Browse all maps of content |

## Active projects

```dataview
TABLE status, area FROM "01_Projects"
WHERE status = "active"
SORT file.mtime DESC
```

## Pinned areas

```dataview
TABLE status FROM "02_Areas"
WHERE status = "active"
SORT file.name ASC
```

## Recent captures

```dataview
TABLE created FROM "00_Inbox"
WHERE type = "capture"
SORT created DESC
LIMIT 10
```

---

> **Getting started:** press `Ctrl/Cmd+P` → *Templater: Create new note from template* to create your first note.  
> Press `Ctrl/Cmd+Shift+P` → *Periodic Notes: Open today's daily note* to open today.
