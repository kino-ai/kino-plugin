<p align="center"><img src="assets/kino.png" width="72" alt="Kino"></p>

<h1 align="center">Kino</h1>

<p align="center">
  <a href=".mcp.json"><img src="https://img.shields.io/badge/MCP-local-0e9fff?style=flat-square" alt="MCP: local"></a>
  <a href=".codex-plugin/plugin.json"><img src="https://img.shields.io/badge/preview-0.1.0-555555?style=flat-square" alt="Preview: 0.1.0"></a>
</p>

<h2 align="center">Media asset management and video editing for your agent.</h2>

<p align="center">Organize and search footage, edit timelines, create motion graphics, export video, and create shareable review links with Kino Pro.</p>

<p align="center">
  <a href="https://kino.ai">Website</a> ·
  <a href="https://kinoai.mintlify.dev/docs">Documentation</a> ·
  <a href="#installation">Installation</a> ·
  <a href="mailto:hello@kino.ai">Support</a>
</p>

## Get started

1. Install Kino for [macOS](https://installer.kino.ai/mac/installer/universal), [Windows](https://installer.kino.ai/windows/nsis/x64), or [Linux](https://installer.kino.ai/linux/deb/x64).
2. Open Kino and sign in. Keep it running on the same computer as your agent.
3. Connect your agent below.

## Installation

<details>
<summary><strong>Codex CLI</strong></summary>

```sh
codex plugin marketplace add https://github.com/kino-ai/kino-plugin.git
codex plugin add kino@kino-plugin
```

Start a fresh conversation.

</details>

<details>
<summary><strong>Claude Code</strong></summary>

```sh
claude plugin marketplace add https://github.com/kino-ai/kino-plugin.git
claude plugin install kino@kino-plugin
```

Start a fresh session and run `/mcp` to inspect the connection.

</details>

<details>
<summary><strong>Cursor</strong></summary>

Add this connection to `~/.cursor/mcp.json` or your project's `.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "kino": {
      "url": "http://127.0.0.1:45680/mcp"
    }
  }
}
```

Restart the agent session.

</details>

<details>
<summary><strong>ChatGPT and Claude Desktop</strong></summary>

In Kino, choose **Install MCP**, select your desktop client, and install the connector.

</details>

<details>
<summary><strong>Grok Bot</strong></summary>

Install Kino on the computer Grok Bot uses for the conversation. For its cloud computer, use the Linux installer and sign in there. Keep Kino running, with Node.js and npm available on that computer.

Add a custom MCP server named `kino`, choose **Command**, and enter:

```sh
npx -y mcp-remote http://127.0.0.1:45680/mcp --allow-http
```

The command runs beside Kino and bridges its local HTTP server to Grok Bot. Ask the bot to call `getKinoInstructions`, then `listProjects`.

If the Debian/Ubuntu installer reports a missing `libsecret-1-0` dependency, install it and retry:

```sh
sudo apt-get update
sudo apt-get install -y libsecret-1-0
```

</details>

## Try it

> List my recent Kino projects.

[MCP tools](https://kinoai.mintlify.dev/docs/mcp/tools) · [Installation checks](TESTING.md)
