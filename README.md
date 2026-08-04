# mcp-data-oregon

Oregon Open Data — US government open data (data.oregon.gov) via the Socrata SoQL API: state agencies, business, health & environment. Keyless.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `datasets` | Search the Oregon Open Data catalog of open datasets by keyword. Returns each dataset's resource_id, name, description, category and update date — pass the resource_id to query/metadata. |
| `query` | Run a Socrata SoQL query against a Oregon Open Data dataset by resource_id (e.g. "tckn-sxa6"). Filter with where/select/group/order (SoQL clauses, without the leading $) plus limit/offset. Returns matching rows as JSON. |
| `metadata` | Get a Oregon Open Data dataset's schema + metadata (columns, types, row count, category, last-updated) by resource_id, e.g. "tckn-sxa6". |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "data-oregon": {
      "url": "https://gateway.pipeworx.io/data-oregon/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Data Oregon data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
