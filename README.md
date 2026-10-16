# scrape.land for AI tools

[scrape.land](https://scrape.land) as a remote [MCP](https://modelcontextprotocol.io) server: your AI assistant can read any web page (past most blocks) as markdown or JSON, search the web, and find local businesses.

- **Endpoint:** `https://scrape.land/mcp` (Streamable HTTP)
- **Auth:** `Authorization: Bearer YOUR_KEY`, with a key from your [dashboard](https://scrape.land/dashboard)
- **Tools:** `fetch_page`, `extract_data`, `web_search`, `find_local_businesses`
- **Billing:** each call uses request units on your plan; blocked and failed calls are free. [Pricing](https://scrape.land/pricing)

## Install

**Claude Code** (this repo is a plugin marketplace):

```bash
claude plugin marketplace add scrape-land/mcp
claude plugin install scrape-land@scrape-land
```

Then set your API key (stored securely): run `/plugin configure scrape-land@scrape-land` in Claude Code, or install with `--config api_key=YOUR_KEY`.

**Gemini CLI:**

```bash
gemini extensions install https://github.com/scrape-land/mcp
```

**Claude (claude.ai, Desktop, mobile):** Settings, Connectors, Add custom connector, URL `https://scrape.land/mcp`, request header `Authorization: Bearer YOUR_KEY`.

**Cursor, VS Code, Windsurf, Zed, Kiro, Cline, OpenAI Agents SDK, Claude API:** copy-paste configs and one-click buttons are in the [docs](https://scrape.land/docs#mcp).

## Privacy and support

- Privacy policy: https://scrape.land/privacy
- Terms: https://scrape.land/terms
- Support: support@scrape.land
