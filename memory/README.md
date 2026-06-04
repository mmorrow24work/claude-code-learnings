# Memory System

Claude Code has a persistent, file-based memory system scoped to each project.

## Location

```
~/.claude/projects/<path-slug>/memory/
```

## Memory types

| Type | Stores |
|------|--------|
| `user` | Who you are, your role, preferences |
| `feedback` | How Claude should (or shouldn't) behave |
| `project` | Goals, deadlines, decisions for this project |
| `reference` | Pointers to external systems (Linear, Grafana, etc.) |

## Format

Each memory is a Markdown file with frontmatter:

```markdown
---
name: short-kebab-slug
description: one-line summary
metadata:
  type: feedback
---

Rule or fact here.

**Why:** reason the user gave  
**How to apply:** when this kicks in
```

`MEMORY.md` in the memory folder is an index — one line per memory, loaded into every conversation.

## Notes

<!-- Add discoveries as you experiment -->
