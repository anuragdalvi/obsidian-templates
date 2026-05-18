---
type: capture
status: active
area: weekly
tags: [weekly-review]
week: <% tp.date.now("YYYY-[W]ww") %>
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
---

# Week <% tp.date.now("ww, YYYY") %>

_<% tp.date.now("YYYY-MM-DD", 0 - tp.date.now("d") + 1) %> – <% tp.date.now("YYYY-MM-DD", 7 - tp.date.now("d")) %>_

## Completed this week

```tasks
done after <% tp.date.now("YYYY-MM-DD", -7) %>
done before <% tp.date.now("YYYY-MM-DD", 1) %>
```

## What went well

- 

## What could be improved

- 

## Open loops (carry forward)

- [ ] 

## Projects check-in

```dataview
TABLE status, area FROM "01_Projects"
WHERE status = "active"
SORT file.mtime DESC
```

## Intentions for next week

1. 
2. 
3. 
