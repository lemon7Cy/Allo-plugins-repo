# Allo Plugin Marketplace

This repository contains installable Allo plugin metadata for MCP and CLI integrations. It is separate from the Allo skills marketplace because plugins can launch executable processes.

## Files

- `plugin-marketplace.json` is the marketplace index consumed by Allo.
- `plugins/*/plugin.json` mirrors each installable plugin entry.
- `plugins/*/README.md` documents command, permissions, and safety notes.

## Configure Allo

Set:

```bash
ALLO_PLUGIN_MARKETPLACE_URL=https://raw.githubusercontent.com/wbz0429/Allo-plugins-repo/main/plugin-marketplace.json
```

Then restart the Allo gateway or packaged Desktop app.

## Safety

Installing a plugin stores metadata only. Allo must not execute MCP or CLI commands during marketplace browsing or installation.
