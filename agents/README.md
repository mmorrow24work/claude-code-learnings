# Agents & Subagents

Claude Code can spawn subagents to parallelize work or isolate context.

## Agent types (built-in)

| Type | Best for |
|------|---------|
| `claude` | General-purpose catch-all |
| `Explore` | Fast read-only codebase search |
| `Plan` | Designing implementation strategy |
| `code-reviewer` | Independent code review |
| `claude-code-guide` | Questions about Claude Code itself |

## Spawning an agent

Use the Agent tool in a prompt, or Claude will spawn one automatically when the task fits.

Key options:
- `isolation: "worktree"` — agent works on an isolated git worktree
- `run_in_background: true` — agent runs in parallel while you continue

## Notes

<!-- Add discoveries as you experiment -->
