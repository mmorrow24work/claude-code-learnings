# Settings & Configuration

## Config files

Precedence (highest to lowest): Managed > Command-line > Local > Project > User

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
    "allow": ["Bash(npm run *)", "Bash(git *)"],
    "deny": ["Read(./.env)"]
  },
  "env": {
    "MY_VAR": "value"
  },
  "hooks": {}
}
```

## Permissions syntax

- `Bash(git *)` — allow all git commands (any arguments)
- `Bash(npm run lint)` — allow exactly this command
- `mcp__github__*` — allow all GitHub MCP tools
- Wildcards (`*`) match any arguments
- **Deny rules always take precedence over allow rules**

Use the `/update-config` skill to add rules without editing JSON manually.

## Reducing permission prompts — permission modes

Press `Shift+Tab` to cycle through four modes:

| Mode | Behavior |
|------|----------|
| **Default** | Asks before file edits and shell commands |
| **Auto-accept edits** | File edits + filesystem commands run without asking; other commands still prompt |
| **Plan mode** | Read-only — Claude plans first, you approve before anything executes |
| **Auto mode** | Background safety checks evaluate actions (preview) |

There is **no blanket skip-permissions flag** — the allow list + mode toggle are the intended path for reducing friction without disabling safety.

## CLAUDE.md for behavioral guidance

`.claude/CLAUDE.md` is read at the start of every session and survives `/compact`. Use it for persistent instructions that should apply across all conversations:

```markdown
Don't ask for confirmation before running tests.
Always run npm test before committing.
Use the existing auth pattern in src/auth/.
```

Put critical rules in the first 200 lines — that's what gets loaded as priority context.

## Notes

<!-- Add discoveries as you experiment -->
