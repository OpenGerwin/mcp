# Contributing to OpenGerwin MCP Servers

Thank you for your interest in contributing! 🎉

## How This Repo Works

This repository (`OpenGerwin/mcp`) is a **showcase/catalog**. Actual server code lives in separate repos:

| Server | Repository |
|---|---|
| Google AI Docs | [OpenGerwin/mcp-google-ai-docs](https://github.com/OpenGerwin/mcp-google-ai-docs) |

## Where to Contribute

### Bug reports & feature requests
→ Open an issue in the **specific server's repo** (see table above).

### New server ideas
→ Open a [Discussion](https://github.com/OpenGerwin/mcp/discussions) in this repo.

### Catalog updates
→ PRs to update this README are welcome.

## Creating a New MCP Server

If you'd like to create a new MCP server under the OpenGerwin organization:

1. **Open a Discussion** describing the server and its use case
2. Follow our design principles:
   - Use `mcp[cli]` SDK
   - Support `stdio` transport (primary) and optionally HTTP
   - Include comprehensive `README.md` with installation instructions
   - Add examples for Claude Desktop, Cursor, and VS Code
   - MIT License
3. Once approved, create the repo and submit a PR to add it to the catalog

## Code Style

- Python: Use `ruff` for formatting and linting
- TypeScript: Use `prettier` + `eslint`
- All: Write clear docstrings and type hints

## License

By contributing, you agree that your contributions will be licensed under MIT.
