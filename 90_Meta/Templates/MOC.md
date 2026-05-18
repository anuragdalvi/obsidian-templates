---
type: moc
status: active
area: <% tp.file.title %>
tags: [moc]
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
---

# <% tp.file.title %> — Map of Content

_This MOC is the entry point for everything related to **<% tp.file.title %>**. Keep it curated; notes live in their folders, links live here._

## Core concepts

- [[]]

## Active projects

```dataview
TABLE status, created FROM "01_Projects"
WHERE area = this.area AND status = "active"
SORT created DESC
```

## Resources & references

- [[]]

## Decisions

```dataview
LIST FROM "02_Areas"
WHERE type = "decision" AND area = this.area
SORT decision-date DESC
```

## Archive

_Notable completed or parked items_
- [[]]
