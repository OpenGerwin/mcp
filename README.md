# 🧩 OpenGerwin MCP Servers

Open-source [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) servers that give AI agents superpowers.

Each server is a standalone package — install only what you need.

---

## Available Servers

| Server | Description | Status | Install |
|---|---|---|---|
| 🔍 **[Google Agent Platform Docs](https://github.com/OpenGerwin/mcp-google-agent-platform-docs)** | Search & read Google AI platform documentation (GEAP + Vertex AI). 3400+ pages. | ✅ Ready | `pip install mcp-google-agent-platform-docs` |
| 🚧 *More coming soon* | Bitrix24, WordPress, and others | Planned | — |

---

## What is MCP?

[Model Context Protocol](https://modelcontextprotocol.io/) is an open standard that lets AI assistants (Claude, Cursor, VS Code Copilot, etc.) connect to external tools and data sources.

Instead of hallucinating API details, your AI can **look up the real documentation** in real-time.

```
┌─────────────────┐     MCP      ┌──────────────────────┐
│  AI Assistant    │◄────────────►│  MCP Server          │
│  (Claude, etc.)  │   (stdio)    │  (your tools + data) │
└─────────────────┘              └──────────────────────┘
```

## Quick Start

### 1. Pick a server from the table above

### 2. Install it

```bash
pip install mcp-google-agent-platform-docs
```

### 3. Connect to your AI client

<details>
<summary><b>Claude Desktop</b></summary>

Add to `claude_desktop_config.json`:
```json
{
  "mcpServers": {
    "google-agent-platform-docs": {
      "command": "mcp-google-agent-platform-docs"
    }
  }
}
```
</details>

<details>
<summary><b>Cursor</b></summary>

Add to `.cursor/mcp.json`:
```json
{
  "mcpServers": {
    "google-agent-platform-docs": {
      "command": "mcp-google-agent-platform-docs",
      "transport": "stdio"
    }
  }
}
```
</details>

<details>
<summary><b>VS Code</b></summary>

Add to `.vscode/mcp.json`:
```json
{
  "mcpServers": {
    "google-agent-platform-docs": {
      "command": "mcp-google-agent-platform-docs",
      "transport": "stdio"
    }
  }
}
```
</details>

---

## Server Details

### 🔍 Google Agent Platform Docs

> **Repo:** [OpenGerwin/mcp-google-agent-platform-docs](https://github.com/OpenGerwin/mcp-google-agent-platform-docs)
> **PyPI:** `pip install mcp-google-agent-platform-docs`

MCP server providing real-time access to Google's AI platform documentation:

- **Gemini Enterprise Agent Platform (GEAP)** — 2300+ pages (current platform)
- **Vertex AI Generative AI** — 1100+ pages (legacy archive)

**Tools:**
| Tool | Description |
|---|---|
| `search_docs` | Full-text search across documentation |
| `get_doc` | Read any documentation page |
| `list_sections` | Browse documentation structure |
| `list_models` | Reference of all available AI models |

---

## Contributing

We welcome contributions! Whether it's:
- 🐛 Bug reports and fixes
- ✨ New MCP server ideas
- 📖 Documentation improvements

Each server has its own repo — please open issues and PRs there.

For general questions or ideas about new servers, use [Discussions](https://github.com/OpenGerwin/mcp/discussions) in this repo.

## License

All servers are released under the [MIT License](LICENSE).

---

<p align="center">
  <b>OpenGerwin</b> — Open-source tools for AI agents
</p>
