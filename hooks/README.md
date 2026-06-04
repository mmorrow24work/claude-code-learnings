# Hooks

Hooks let you run shell commands automatically in response to Claude Code events.
Configured in `settings.json` under the `hooks` key.

## Hook events

| Event | Fires when |
|-------|-----------|
| `PreToolUse` | Before Claude calls a tool |
| `PostToolUse` | After a tool call completes |
| `UserPromptSubmit` | When you submit a message |
| `Stop` | When Claude finishes a turn |

## Example

```json
{
  "hooks": {
    "Stop": [
      {
        "matcher": "",
        "hooks": [
          { "type": "command", "command": "notify-send 'Claude is done'" }
        ]
      }
    ]
  }
}
```

## Notes

<!-- Add discoveries as you experiment -->
