# GQLens Cursor Plugin

Cursor Marketplace plugin for [GQLens](https://gqlens.com) — GraphQL schema intelligence MCP server.

## Structure

```
plugins/
  gqlens/
    .cursor-plugin/plugin.json   # Plugin metadata
    mcp.json                     # MCP server configuration
    assets/logo.svg              # Plugin logo
    README.md                    # Plugin documentation
```

## Development

Validate the plugin structure:

```bash
node scripts/validate-template.mjs
```

## Submission

Submit to the Cursor Marketplace by providing a link to this repository at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish).
