---
type: resource
status: active
area: meta
tags: [playbook, obsidian, prompt-engineering]
created: 2026-05-18
updated: 2026-05-18
---

# Generate a Portable Obsidian Vault — Prompt Playbook

Use this prompt with Claude Code (or any capable coding agent) to regenerate or reseed this vault for a new topic.

## The Prompt

```
You are an experienced Obsidian power-user and knowledge-management practitioner.
Build me a portable, opinionated Obsidian starter vault on disk that I can copy
or clone to seed a new vault for any topic. The vault must be usable immediately
after `Open folder as vault` in Obsidian — no manual setup.

Target path: /path/to/My-New-Vault
Framework: PARA + LYT Maps of Content
Plugins: dataview, omnisearch, obsidian-linter, periodic-notes,
         obsidian-advanced-uri, url-into-selection, obsidian-git,
         obsidian-tasks-plugin, templater-obsidian,
         obsidian-excalidraw-plugin, mermaid-tools
Theme (default): VSCode Dark Modern  (also bundle: Minimal, AnuPpuccin, Things)
Templates: Capture, Project-RFC, Learning, Daily-Note, Weekly-Review,
           Meeting, Decision, Runbook, MOC
Git: init with local user only (vault@local); do NOT push.
```

## Notes on using it

- **Plugin-install is the brittlest step.** Use the fallback ladder:
  `releases/latest/download` → GitHub API → `raw.githubusercontent.com/main`.
  If a plugin still fails, record it in the README and move on.
- **Pin versions for reproducibility.** Replace `releases/latest/download`
  with `releases/download/<tag>/` and specify the tag per plugin.
- **Swap plugins for different use-cases:**
  - Kanban: add `mgmeyers/obsidian-kanban`
  - Spaced repetition: add `st3v3nmw/obsidian-spaced-repetition`
  - Long-form writing: swap Tasks/Dataview/Linter for `kevboh/longform`

## Folder skeleton

```
00_Inbox/
  Daily/
  Weekly/
01_Projects/
02_Areas/
03_Resources/
  Playbooks/
04_Archive/
05_MOCs/
90_Meta/
  Templates/
90_Personal/    ← excluded from git and linter
```
