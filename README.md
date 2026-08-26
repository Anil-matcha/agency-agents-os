# Agency Agents OS

**An open ecosystem of specialized AI agents for real business work.**

Discover agents for video, image, and voice production, SEO, social media, advertising, sales, research, analytics, and more — powered by real APIs, not just prompts.

Agency Agents OS is a curated directory of AI agents, organized as broad, focused **umbrella repositories** (one per capability area) rather than hundreds of one-off micro-repos. Each umbrella repo bundles several related sub-agents so it's easy to browse, easy to maintain, and actually rankable on GitHub search.

This project is independent of, but built to work with, the [Muapi API](https://muapi.ai) — a unified API for 500+ generative-media models (video, image, voice, audio, 3D). Agents here reference Muapi's public API surfaces for execution; no Muapi source code or private implementation details live in this catalog.

## Why umbrella repos, not micro-repos

A directory of 100+ single-purpose repos (`email-verification-agent`, `funding-signals-agent`, ...) is hard to browse, duplicates maintenance overhead, and doesn't rank for anything. Instead, each umbrella repo is a broad, high-search-volume category (e.g. "AI video agent," "AI SEO agent") that houses several narrower sub-agents as sections inside itself. A sub-agent is promoted to its own umbrella only once its own search volume and capability set justify it.

## Categories

| Category | Umbrella repo | Status |
|---|---|---|
| Video production | [`ai-video-agent`](https://github.com/SamurAIGPT/ai-video-agent) | Blueprint |
| Image / creative production | [`ai-image-agent`](https://github.com/SamurAIGPT/ai-image-agent) | Blueprint |
| Voice, narration, dubbing, calling | [`ai-voice-agent`](https://github.com/SamurAIGPT/ai-voice-agent) | Blueprint |
| SEO / organic growth | [`ai-seo-agent`](https://github.com/SamurAIGPT/ai-seo-agent) | Blueprint |
| Answer/generative-engine optimization (AEO/GEO) | [`ai-aeo-geo-agent`](https://github.com/SamurAIGPT/ai-aeo-geo-agent) | Blueprint |
| Social media management | [`ai-social-agent`](https://github.com/SamurAIGPT/ai-social-agent) | Blueprint |
| Content repurposing / clipping | [`ai-content-repurposing-agent`](https://github.com/SamurAIGPT/ai-content-repurposing-agent) | Blueprint |
| Marketing (email, campaigns, product) | [`ai-marketing-agent`](https://github.com/SamurAIGPT/ai-marketing-agent) | Coming Soon |
| Paid media (PPC, paid social, programmatic) | [`ai-ads-agent`](https://github.com/SamurAIGPT/ai-ads-agent) | Coming Soon |
| E-commerce / CRO | [`ai-ecommerce-agent`](https://github.com/SamurAIGPT/ai-ecommerce-agent) | Coming Soon |
| Sales / lead generation | [`ai-sales-agent`](https://github.com/SamurAIGPT/ai-sales-agent) | Coming Soon |
| Research / audience & market research | [`ai-research-agent`](https://github.com/SamurAIGPT/ai-research-agent) | Coming Soon |
| Analytics / reporting | [`ai-analytics-agent`](https://github.com/SamurAIGPT/ai-analytics-agent) | Coming Soon |
| Competitive intelligence | [`ai-competitor-intelligence-agent`](https://github.com/SamurAIGPT/ai-competitor-intelligence-agent) | Coming Soon |
| Reputation / PR / brand monitoring | [`ai-reputation-agent`](https://github.com/SamurAIGPT/ai-reputation-agent) | Coming Soon |

A "Blueprint" umbrella means at least one sub-agent inside it is built on a live Muapi API — check that repo's own README for which specific sub-agents are live vs. still Coming Soon.

See [`categories/`](categories/) for a longer description of each grouping, or jump straight into a repo above.

## Status labels

Every agent in this catalog carries one of these labels so you can judge maturity before you build on it:

- **Coming Soon** — instructions are drafted, but the agent depends on a Muapi API capability that isn't live yet.
- **Blueprint** — complete instructions and workflow, backed by live APIs, but not yet verified end-to-end.
- **Tested** — the workflow has been run against the stated APIs.
- **Live** — a public demo or hosted implementation exists.
- **Open Source** — a runnable or independently usable implementation is available.
- **Deprecated** — the API or workflow is no longer supported.

## How an agent repo is structured

Every umbrella repo follows the same shape:

```text
ai-<category>-agent/
├── README.md              # what this category covers, why it's here
├── agents/
│   └── <sub-agent>/
│       └── SKILL.md        # the canonical, runtime-agnostic instruction file
├── examples/
└── LICENSE
```

`SKILL.md` is a Markdown instruction file any LLM runtime — a hosted agent, an MCP client, a custom app — can load directly. No application code is required.

## Using an agent

1. Open the umbrella repo for the category you need.
2. Read the sub-agent's `SKILL.md` for its mission, required inputs, and workflow.
3. Get a Muapi API key at [muapi.ai](https://muapi.ai) if the agent needs live execution (media generation, data lookups, etc.).
4. Load the `SKILL.md` into your agent runtime of choice, or follow it manually.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Short version: propose an agent, follow the template, describe the APIs it needs honestly, and open a PR — either as a new sub-agent inside an existing umbrella repo, or as a link to your own high-quality external repo.

## License

[MIT](LICENSE)
