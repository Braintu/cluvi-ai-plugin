# Cluvi AI for AI assistants

<img src="assets/logo.png" width="96" height="96" alt="Cluvi AI logo">

Cluvi AI is the AI receptionist for restaurants, built in partnership with Cluvi. It answers guests on WhatsApp, Instagram, the phone and your website, takes reservations and delivery orders, and hands the conversation to your team when a person is needed. Connect it to run your restaurant's Cluvi AI workspace in plain language.

What you can do:
- Find what guests asked about, by topic, guest, channel or date, with a link to each conversation.
- Follow delivery orders: accept or reject a new order, move it along, assign a courier and tell the guest about their order.
- Mark a dish sold out for the night, or take it off the menu.
- Read the day's reservations and change one: confirm, seat, cancel or move it.
- Read the delivery report: sales, best-selling dishes, busy hours and late deliveries.
- Count and compare conversations and orders, and see the numbers as charts.
- Train the AI receptionist: its Instructions, Q&A and knowledge files, and your promotions.
- Run the team: invite people, change roles, set opening hours and choose who replies, the AI receptionist or your team.

How it works:
You sign in with your Cluvi AI account and choose one workspace. Reading is always on; making changes is a separate permission you can leave off. Cluvi AI can do only what your role allows. Kitchen actions, such as accepting an order, run when you ask, as they do on the kitchen screen. Before an important change, such as editing the AI receptionist, changing a reservation or removing dishes, Cluvi AI shows you a preview and applies the change only after you say yes in the chat.

Limitations:
Requires a Cluvi AI account. One connection reaches one workspace. Cluvi AI does not take payments or send refunds.

**Server URL:** `https://cluvi.ai/mcp` (remote MCP server, Streamable HTTP). There is no API key: the first time, your assistant opens Cluvi AI in the browser for you to sign in. Disconnect it anytime in Cluvi AI, in Settings under Account.

## Install

### Cursor

Install Cluvi AI from the Cursor Marketplace, or add the server to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "cluvi": {
      "url": "https://cluvi.ai/mcp"
    }
  }
}
```

### Grok Bot

Grok Bot installs apps from the Cursor Marketplace: open Connect apps, find Cluvi AI and choose Add.

### Gemini CLI

```sh
gemini extensions install https://github.com/Braintu/cluvi-ai-plugin
```

Then run `/mcp auth cluvi` in Gemini CLI to sign in.

### Claude Code

```sh
claude mcp add --transport http --scope user cluvi https://cluvi.ai/mcp
claude mcp login cluvi
```

### Codex

```sh
codex mcp add cluvi --url https://cluvi.ai/mcp
codex mcp login cluvi
```

### Claude (web, desktop and mobile)

Settings, Connectors, Add custom connector. Paste `https://cluvi.ai/mcp` and choose Connect.

### ChatGPT

Turn on developer mode in Settings, then add `https://cluvi.ai/mcp` as a custom MCP server under Plugins.

### Any other assistant

Add `https://cluvi.ai/mcp` as a remote MCP server. The full guide covers more apps: [cluvi.ai/mcp](https://cluvi.ai/mcp), and its version for AI assistants: [cluvi.ai/mcp.md](https://cluvi.ai/mcp.md).

## What this repository contains

Nothing here runs on your computer: every file only points your assistant at `https://cluvi.ai/mcp`.

| File | What it is |
| --- | --- |
| `.cursor-plugin/plugin.json` | The plugin manifest for Cursor and Grok Bot |
| `mcp.json` | The server address, for Cursor |
| `gemini-extension.json` | The extension manifest for Gemini CLI |
| `GEMINI.md` | Short instructions Gemini CLI gives the AI model |
| `assets/logo.png` | The Cluvi AI logo |

## Help, privacy and terms

- Help: [cluvi.ai/help](https://cluvi.ai/help) or support@cluvi.ai
- Privacy policy: [cluvi.ai/privacy](https://cluvi.ai/privacy)
- Terms of service: [cluvi.ai/terms](https://cluvi.ai/terms)

## License

The files in this repository are released under the [MIT License](LICENSE). Cluvi AI is operated by Braintu Inc. in partnership with Cluvi. The Cluvi AI and Cluvi names and logos belong to their owners; this license grants no right to use them.
