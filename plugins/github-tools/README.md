# GitHub Tools

GitHub MCP plugin for repository operations.

## Command

`npx -y @modelcontextprotocol/server-github`

## Required Environment

- `GITHUB_TOKEN`

## Permissions

- github-api
- network
- repository-metadata
- repository-write

## Safety

Installing this plugin does not validate or use `GITHUB_TOKEN`. Runtime launch must check credentials and user intent.
