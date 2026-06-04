# MCP — Model Context Protocol

MCP servers extend Claude Code with new tools (e.g., GitHub, databases, Slack).

## Adding an MCP server

```bash
claude mcp add <name> -- <command> [args...]
# or for SSE servers:
claude mcp add --transport sse <name> <url>
```

## Useful servers

| Server | What it provides |
|--------|----------------|
| `@anthropic-ai/mcp-server-github` | GitHub issues, PRs, code search |
| `@modelcontextprotocol/server-filesystem` | File system access |
| `@modelcontextprotocol/server-postgres` | PostgreSQL queries |

## Notes

<!-- Add discoveries as you experiment -->
