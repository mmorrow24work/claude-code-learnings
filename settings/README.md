# Settings & Configuration

## Config files (precedence: project > local > user > global)

| File | Scope |
|------|-------|
| `~/.claude/settings.json` | User-global |
| `.claude/settings.json` | Project (checked into git) |
| `.claude/settings.local.json` | Project-local (gitignored) |

## Key settings

```json
{
  "model": "claude-opus-4-8",
  "theme": "dark",
  "permissions": {
    "allow": ["Bash(npm:*)", "Bash(git:*)"],
    "deny": []
  },
  "env": {
    "MY_VAR": "value"
  },
  "hooks": {}
}
```

## Permissions syntax

- `Bash(npm:*)` — allow all npm commands
- `Bash(git log:*)` — allow git log with any args
- `mcp__github__*` — allow all GitHub MCP tools

## Notes

<!-- Add discoveries as you experiment -->
