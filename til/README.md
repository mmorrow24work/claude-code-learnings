# TIL — Today I Learned

Short dated entries for quick discoveries.

## Template

```markdown
## YYYY-MM-DD — <short title>

<1-3 sentences describing what you learned and why it matters>
```

---

## 2026-06-04 — Reducing permission prompts

Use `Shift+Tab` to cycle permission modes (default → auto-accept edits → plan mode → auto). For finer control, add `permissions.allow` rules to `settings.json` — e.g. `"Bash(git *)"` pre-approves all git commands. There's no blanket skip flag; the allow list is the intended path. CLAUDE.md is the place for persistent behavioral instructions that survive `/compact`.

## 2026-06-04 — /context shows context window usage

`/context` renders a colored grid of what's consuming your context window (history, memory, tools, etc.) with optimization suggestions and capacity warnings. Add `all` for the full breakdown. Useful before deciding to `/compact` or `/clear`.

## 2026-06-04 — Created this repo

Started capturing Claude Code learnings. Repo scaffolded with topic folders for cli, hooks, mcp, agents, memory, and settings.
