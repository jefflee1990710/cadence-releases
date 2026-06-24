# Cadence — Releases

Public download & auto-update artifacts for **Cadence** (design tooling for
agents, not humans). The application source is private; only build outputs are
published here.

## Download the app

Permanent links (always serve the latest published version):

| Platform | Download |
|---|---|
| macOS (Apple Silicon) | [Cadence-arm64.dmg](../../releases/latest/download/Cadence-arm64.dmg) |
| macOS (Intel) | [Cadence-x64.dmg](../../releases/latest/download/Cadence-x64.dmg) |
| Windows | [Cadence-setup.exe](../../releases/latest/download/Cadence-setup.exe) |

Or browse the **[latest release](../../releases/latest)**. The app
**auto-updates itself** (via `electron-updater`) — you only download once.

## Standalone MCP binaries (no Node required)

To drive Cadence from an AI agent (Cursor, Claude Desktop, Windsurf, …) without
installing Node, grab the binary for your OS from the
**[`mcp-v*` pre-release](../../releases?q=mcp)**:

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `cadence-mcp-mac-arm64` |
| macOS (Intel) | `cadence-mcp-mac-x64` |
| Windows | `cadence-mcp-win.exe` |
| Linux | `cadence-mcp-linux` |

Then point your MCP client's command at the binary with empty args:

```json
{ "mcpServers": { "cadence": { "command": "/path/to/cadence-mcp-mac-arm64", "args": [] } } }
```

> The Cadence app must be running before any tool call — the MCP server is a thin
> shim to the live app over a local socket.

For Claude Code, install the bundled plugin instead (tools **+** a
design-and-verify skill). See the in-app **Integration** tab for per-client steps.
