# Memocore MCP

Remote [Model Context Protocol](https://modelcontextprotocol.io/) server for [Memocore](https://memocore.ai).

Memocore is cloud memory for AI agents and teams. Your agent saves decisions, project details and how your team works, then finds them again in the next chat. The same memory is available in Claude, ChatGPT, Cursor and any other AI tool connected to your account, and a team can share one memory across all its agents.

The server is hosted by Memocore, so there is nothing to install or run.

## Server

- URL: `https://memocore.ai/mcp`
- Transport: Streamable HTTP
- Auth: OAuth. No API keys to paste: your AI tool opens the Memocore sign-in page when it connects.

A Memocore account is required. The free plan is enough to start, and you can sign up during the first sign-in.

## Setup

### VS Code (GitHub Copilot)

Add the server to `.vscode/mcp.json`:

```json
{
	"servers": {
		"memocore": {
			"type": "http",
			"url": "https://memocore.ai/mcp"
		}
	}
}
```

Start the server and sign in to Memocore when VS Code asks. The tools are then available in Copilot Chat agent mode.

### Cursor

Add the server with one click from [cursor.directory](https://cursor.directory/plugins/memocore).

### Other clients

For clients that use the `mcpServers` config:

```json
{
	"mcpServers": {
		"memocore": {
			"type": "http",
			"url": "https://memocore.ai/mcp"
		}
	}
}
```

Setup guides for Claude, ChatGPT and other AI tools: https://memocore.ai/mcp

## What agents can do

| Category | Capabilities |
| --- | --- |
| Memos | Save private or project memos, search them by meaning and keywords, read, update, delete and restore, view change history |
| Projects | Find, read, create and update shared projects, query rows in table projects |
| Tags | Find, create, update and delete tags |
| Files | Attach files to memos and get download links |
| Sharing | Share a project memo by link and open memocore.ai/m/ links |

## Try it

- "Remember that we only deploy on Fridays after QA sign-off"
- "What did we decide about retrying failed payments?"
- "Save this as a memo in the Backend project"

## Links

- Website: https://memocore.ai
- Setup for other AI tools: https://memocore.ai/mcp
- Help: https://memocore.ai/help
- Privacy: https://memocore.ai/privacy
- Support: support@memocore.ai

## License

MIT