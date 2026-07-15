# OpenCompany Documentation

Official documentation for [OpenCompany](https://github.com/zeenie-ai/opencompany) - an open-source, plugin-first workflow automation platform with AI agents, a React Flow canvas, and a Temporal-backed execution engine.

**110+ nodes across 28 categories** | **12 chat-model providers** | **Dracula theme**

## Live Docs

https://docs.zeenie.xyz/

## Local Development

Built with [Mintlify](https://mintlify.com). The `mint` CLI serves the site from `docs.json`.

```bash
# Install the Mintlify CLI
npm install -g mint

# Run the local dev server (from this folder)
mint dev
```

The docs are served at http://localhost:3000. (The legacy `mintlify` CLI still works as an alias: `mintlify dev`.)

## Documentation Coverage

Navigation is defined in `docs.json`.

### Getting Started

`introduction` · `installation` · `quickstart` · `architecture`

### Node Catalog (`nodes/`)

The live node count is large (~118 node plugins across 28 categories) and grows as plugins are added, so the docs group nodes by category rather than pinning a fixed total.

| Page | Covers |
|------|--------|
| [overview](nodes/overview.mdx) | How the palette is organized; all node categories |
| [ai-models](nodes/ai-models.mdx) | 12 chat-model providers: OpenAI, Anthropic, Gemini, OpenRouter, xAI, Groq, Cerebras, DeepSeek, Kimi, Mistral, Ollama, LM Studio |
| [ai-agent](nodes/ai-agent.mdx) | AI Agent, Chat Agent (Zeenie), memory, and the 16 specialized agents |
| [skills](nodes/skills.mdx) | Master Skill + the built-in skill library |
| [tools](nodes/tools.mdx) | AI tool nodes (calculator, time, search, write-todos, agent builder, dual-purpose tools) |
| [whatsapp](nodes/whatsapp.mdx) | WhatsApp send / query / receive |
| [android](nodes/android.mdx) | 16 Android service nodes |
| [documents](nodes/documents.mdx) | RAG pipeline: scrape / download / parse / chunk / embed / vector store |
| [webhooks](nodes/webhooks.mdx) | Webhook, HTTP, and trigger nodes |
| [schedulers](nodes/schedulers.mdx) | Timer + cron scheduler |

Other node families (Telegram, Twitter/X, Social, Email, Stripe, Browser, Scraper, Filesystem, Code executors, Proxy, Location, Google Workspace) are introduced on the [overview](nodes/overview.mdx) page. For the authoritative, always-current model list per provider, see [ai-models](nodes/ai-models.mdx).

### Tutorials (`tutorials/`)

`first-workflow` · `ai-agent-workflow` · `whatsapp-automation` · `android-automation`

### Deployment (`deployment/`)

- [production](deployment/production.mdx) - recommended path (`company deploy up --provider gcp`: cloud CLI + Terraform + single-port `company serve` under systemd)

### FAQ

`faq`

## Structure

```
docs-OpenCompany/
├── docs.json           # Mintlify config + navigation (Dracula theme)
├── introduction.mdx
├── installation.mdx
├── quickstart.mdx
├── architecture.mdx
├── faq.mdx
├── tutorials/          # 4 step-by-step guides
├── nodes/              # 10 node-category pages
├── deployment/         # production (company deploy)
├── .github/workflows/  # Validation (deploys via the Mintlify GitHub app)
└── logo/
```

## Theme

Dracula palette (defined in `docs.json`):

- Primary `#BD93F9` (purple) · Light `#FF79C6` (pink) · Dark `#6272A4`
- Code blocks: Dracula (dark) / GitHub Light (light)

## Contributing

1. Edit the `.mdx` files - keep facts in sync with the OpenCompany code (models, node names, CLI commands).
2. Preview locally with `mint dev`.
3. Commit and push to `main` - GitHub Actions auto-deploys the site.

## Mintlify Components

`<Card>` / `<CardGroup>`, `<Tabs>` / `<Tab>`, `<Accordion>`, `<Info>` / `<Warning>` / `<Tip>` / `<Check>`, `<ParamField>`, `<Steps>`.

See the [Mintlify docs](https://mintlify.com/docs) for the full component reference.
