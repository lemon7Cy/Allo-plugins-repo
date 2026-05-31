# Filesystem Tools

Workspace-bounded filesystem MCP plugin.

## Command

`npx -y @modelcontextprotocol/server-filesystem $ALLO_WORKSPACE_PATH`

## Permissions

- filesystem-read
- filesystem-write
- workspace-only

## Safety

`ALLO_WORKSPACE_PATH` is injected by Allo at runtime. Never point this plugin at the user's home directory or filesystem root.
