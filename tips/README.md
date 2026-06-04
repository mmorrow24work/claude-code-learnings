# Tips & Tricks

Miscellaneous discoveries that don't fit a single category.

## General

- Type `! <command>` in the prompt to run a shell command inline and have the output land in the conversation.
- `/code-review ultra` triggers a deep multi-agent cloud review of the current branch.
- `/code-review ultra <PR#>` reviews a specific GitHub PR.
- Claude reads `CLAUDE.md` at project root automatically — use it for persistent project context.

## Context management

- Use `/clear` when context gets long and you're starting a new task.
- Subagents with `isolation: "worktree"` start cold — give them a self-contained prompt.

## Notes

<!-- Add discoveries as you experiment -->
