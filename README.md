# Vault MCP Suite 🔒

**Privacy-first [MCP](https://modelcontextprotocol.io) servers for AI agents.** A family of small, focused tools that let Claude, ChatGPT Apps, or any MCP host work with files **on the user's own machine** — nothing is ever uploaded. No account, no cloud, no tracking.

Each server is free to use for its core tools, with an optional **one-time crypto Pro** unlock (9 USDC on Base, no subscription) for power features. The Pro license is an offline ECDSA-signed token, verified locally — it never phones home.

## The servers

| Server | What it does | Install |
|---|---|---|
| [vaultpdf-mcp](https://github.com/AlexeySamosadov/vaultpdf-mcp) | PDF: merge, split, images→pdf, info · *Pro:* watermark, rotate, delete pages | `npx github:AlexeySamosadov/vaultpdf-mcp` |
| [vaultimg-mcp](https://github.com/AlexeySamosadov/vaultimg-mcp) | Image: info, resize, convert, strip EXIF · *Pro:* watermark, crop, rotate | `npx github:AlexeySamosadov/vaultimg-mcp` |
| [vaultdata-mcp](https://github.com/AlexeySamosadov/vaultdata-mcp) | CSV/JSON: info, convert, stats, filter · *Pro:* sort, dedupe, select | `npx github:AlexeySamosadov/vaultdata-mcp` |
| [vaulttext-mcp](https://github.com/AlexeySamosadov/vaulttext-mcp) | Text: stats, extract, replace, case · *Pro:* redact PII, sort/dedupe lines | `npx github:AlexeySamosadov/vaulttext-mcp` |
| [vaultarchive-mcp](https://github.com/AlexeySamosadov/vaultarchive-mcp) | Zip: create, list, extract · *Pro:* extract-one, add-to-zip | `npx github:AlexeySamosadov/vaultarchive-mcp` |
| [vaulthash-mcp](https://github.com/AlexeySamosadov/vaulthash-mcp) | Integrity: hash, verify, compare · *Pro:* dir manifest, find duplicates | `npx github:AlexeySamosadov/vaulthash-mcp` |
| [vaultjson-mcp](https://github.com/AlexeySamosadov/vaultjson-mcp) | JSON: validate, format, query-by-path · *Pro:* deep-merge, diff | `npx github:AlexeySamosadov/vaultjson-mcp` |
| [vaultqr-mcp](https://github.com/AlexeySamosadov/vaultqr-mcp) | QR: PNG, SVG · *Pro:* Wi-Fi join codes, batch | `npx github:AlexeySamosadov/vaultqr-mcp` |
| [vaultmd-mcp](https://github.com/AlexeySamosadov/vaultmd-mcp) | Markdown: to-HTML, TOC, links · *Pro:* strip-to-text, frontmatter | `npx github:AlexeySamosadov/vaultmd-mcp` |

## Use in Claude Desktop
Add any of them to `claude_desktop_config.json`, e.g.:
```json
{
  "mcpServers": {
    "vaultpdf": { "command": "npx", "args": ["github:AlexeySamosadov/vaultpdf-mcp"] },
    "vaultimg":  { "command": "npx", "args": ["github:AlexeySamosadov/vaultimg-mcp"] }
  }
}
```

## Why local-first?
Agents increasingly handle people's real documents, images, and data. Routing those through a cloud service to merge a PDF or strip EXIF from a photo is needless exposure. The Vault suite does the work **where the files already are** — on the user's machine — so private data stays private.

## Pro & payment
Every server's free tools work forever. To unlock a server's Pro tools, send **9 USDC on Base** to `0xe339997037C7e1C81829fA3e110d3e82B4bDd48E`, open an issue on that server's repo with the tx hash + your email, and a bot verifies the payment on-chain and replies with your license key. One-time, no subscription.

MIT licensed.
