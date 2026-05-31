# Filesystem Tools

Workspace-bounded filesystem MCP plugin.

## Command

`npx -y @modelcontextprotocol/server-filesystem $ALLO_WORKSPACE_PATH`

## Required Environment

- `ALLO_WORKSPACE_PATH`

## Permissions

- filesystem-read
- filesystem-write
- workspace-only

## Safety

Only launch this plugin with `ALLO_WORKSPACE_PATH` set to the active workspace. Never point it at the user's home directory or filesystem root.
