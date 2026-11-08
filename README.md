# Vaultic

**Persistent, private memory for any MCP-compatible AI agent.**

Transcripts, searchable memories, a knowledge graph, and a relationship ledger — all in one local SQLite file on your own machine. No cloud, no telemetry, no account.

[![Launch Llama Tools](https://tools.launchllama.co/featured-badge.png?v=2)](https://tools.launchllama.co/products/vaultic?utm_source=badge&utm_medium=referral)

## What it does

Vaultic is an MCP server that gives any MCP-compatible AI agent a memory that survives between sessions. It stores four kinds of data:

| Kind | What it is |
|------|-----------|
| **Transcripts** | Raw, verbatim conversation record. Append-only. |
| **Memories** | Distilled facts, preferences, summaries and events, found with hybrid search and de-duplicated automatically. |
| **Knowledge graph** | Named entities, typed relations and free-text observations. |
| **Relationship ledger** | What the agent believes about the user, itself and the relationship, each claim linked to its evidence. |

Plus: commitments and repairs tracking, reflections, working state, boundaries, intentions, sentiment hypotheses, artifact storage, retention policies, and a full audit log.

## 108 tools across 5 packs

| Pack | Tools | What it covers |
|------|-------|---------------|
| **core** | 31 | Transcripts, memory CRUD, recall, knowledge graph, reflections, commitments, repairs, sentiment, working state, session lifecycle |
| **memory** | 18 | Conversation history, consolidation, extraction rules, agent profiles, user profiles, tags, intentions, learning proposals |
| **graph** | 12 | Graph reads, temporal queries, evidence provenance, episode tracking, conflict detection, contamination checks |
| **artifacts** | 10 | File/image storage with versioning, experience short-term memory, quarantine and producer management |
| **admin** | 37 | Backup/restore, import/export, retention policies, consent management, boundaries, search index, diagnostics, persona deletion |

Your agent sees 31 core tools by default and reaches the rest through a built-in menu, so they don't fill its context window.

## Key features

- **Local-first** — everything lives in a single SQLite file on your device
- **Encrypted at rest** — AES-256-GCM before anything touches disk
- **Personas** — each agent gets its own identity, goals, values, and memory, scoped by user
- **Nothing silently overwritten** — corrections refute and replace, forgetting archives, commitments are tracked
- **Hybrid search** — semantic (meaning-based) + encrypted keyword search
- **Automatic de-duplication** — new memories checked against existing ones
- **Works offline** — embedded model included, no external API calls needed
- **Audit log** — append-only record of every read and write
- **Standard MCP** — stdio transport (HTTP also available), works with Claude, any MCP client

## Requirements

- Linux (Windows coming soon, macOS untested)
- Python 3.12+ with SQLite 3.51.3+ (install guide uses `uv` with Python 3.13)
- Internet connection once at install time, then fully offline

## Getting started

After purchase, install with pip using the included step-by-step instructions, then register globally:

```json
{
  "mcpServers": {
    "vaultic": {
      "command": "vaultic-mcp"
    }
  }
}
```

Your download includes an **Agent Manual** written to your AI agent, covering all 108 tools, triggers, hooks and skills, plus a rulebook skill and reference hooks for Claude Code.

## Pricing

**€135 one-off.** No subscription, no recurring fees. All 0.x updates included. 14-day refund policy.

**[Buy Vaultic →](https://morrisonsaisolutions.lemonsqueezy.com/checkout/buy/6b51fced-3ffa-4a02-8e04-1caddf4cd045)**

## Honest limitations

- Back up your encryption keys — we can't recover them
- Keyword search matches whole words only (no stemming or prefix)
- Relationship safety check is a pattern list, not a semantic classifier
- De-duplication and decay are heuristics, not verified understanding
- Built for one local user, not multi-tenant
- File-permission hardening tested on Linux only

[See our recall benchmark results →](https://morrisonsaisolutions.ie/benchmarks/)

## Links

- **Website:** [morrisonsaisolutions.ie](https://morrisonsaisolutions.ie/)
- **Product page:** [morrisonsaisolutions.ie/products/vaultic/](https://morrisonsaisolutions.ie/products/vaultic/)
- **Support:** [morrisonsaisolutions.ie/support/](https://morrisonsaisolutions.ie/support/)

## License

Vaultic is commercial software. See the [EULA](https://morrisonsaisolutions.ie/legal/eula/) for terms.

Built by [Morrisons AI Solutions](https://morrisonsaisolutions.ie/).
