---
type: moc
status: active
area: meta
tags: [moc, index]
created: 2026-05-18
updated: 2026-05-18
---

# 000 · Master Index

_All Maps of Content in this vault. Each MOC is the entry point for one area or topic._

## Create a new MOC

1. Create a note in `05_MOCs/` using the **MOC** template
2. Link it from [[Home]] and from this index

## MOC List

```dataview
TABLE area, status FROM "05_MOCs"
WHERE type = "moc" AND file.name != "000-Index"
SORT file.name ASC
```

## By area

```dataview
LIST FROM "05_MOCs"
WHERE type = "moc"
GROUP BY area
```
