# GEO Checklist

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![GEO](https://img.shields.io/badge/GEO-Audit_Checklist-0176d3)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

A technical audit checklist for **Generative Engine Optimization (GEO)** — the practice of optimizing digital presence for visibility in AI-generated responses from ChatGPT, Gemini, Perplexity, Copilot, and other generative engines.

This is not a theoretical framework. It is a practitioner's checklist, built from real audits across e-commerce, SaaS, personal brands, and service businesses.

---

## Table of Contents

- [What is GEO?](#what-is-geo)
- [How to Use This Checklist](#how-to-use-this-checklist)
- [The Checklist](#the-checklist)
- [Examples](#examples)
- [Contributing](#contributing)
- [Maintenance](#maintenance)
- [Citation](#citation)
- [Ecosystem](#ecosystem)
- [License](#license)

## What is GEO?

Generative Engine Optimization is the discipline of structuring your digital presence so that large language models:

1. **Know you exist** — your entity is present in training data and retrieval sources
2. **Understand what you are** — your entity attributes are consistent and machine-readable
3. **Cite you accurately** — your content is structured for extraction and attribution
4. **Recommend you** — your authority signals are strong enough to surface in relevant queries

GEO is not a replacement for SEO. It is a complementary discipline that addresses a different discovery surface: AI-generated answers instead of search engine results pages.

## How to Use This Checklist

1. Open [`checklist.md`](checklist.md) for the full technical checklist
2. Work through each section systematically
3. Use the examples in [`examples/`](examples/) for industry-specific guidance
4. Track your progress by copying the checklist into your project management tool

**Priority levels:**

- **P0** — Critical. Do this first. Direct impact on AI visibility.
- **P1** — Important. Significant impact on entity understanding.
- **P2** — Recommended. Improves consistency and long-term visibility.

## The Checklist

The complete checklist is in [`checklist.md`](checklist.md). It covers seven domains:

| Domain | Items | Focus |
|---|---|---|
| Schema Markup | 12 | Structured data for entity definition |
| llms.txt | 6 | AI-specific discoverability file |
| Entity Consistency | 10 | Cross-platform alignment |
| Citation Signals | 8 | Content structure for AI citation |
| Multi-Platform Presence | 7 | Distribution and authority signals |
| Content Structure | 9 | Machine-readable content patterns |
| Monitoring | 6 | Tracking AI visibility over time |

## Examples

Industry-specific guidance with concrete implementations:

- [E-commerce](examples/ecommerce.md) — product entities, review markup, catalog optimization
- [SaaS](examples/saas.md) — software entities, feature documentation, comparison positioning
- [Personal Brand](examples/personal-brand.md) — person entities, expertise signals, publication markup

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Issues, suggestions, and pull requests are welcome.

## Maintenance

`checklist.md` is the source of truth. The domain table above and the Summary Scorecard at the end of the checklist must agree; on 30 September 2026 both count 58 items (19 P0, 23 P1, 16 P2), and a pull request that adds or removes an item updates both.

The `qualidade` workflow in `.github/workflows/qualidade.yml` runs markdownlint (rules in `.markdownlint-cli2.jsonc`) and the lychee link checker on every push to `main` and every pull request. It also runs every Monday at 09:00 UTC, so an external reference that dies is flagged within a week even when nobody touches the repository.

The quarterly roadmap lives in [`docs/ROADMAP_2026Q2-Q4.md`](docs/ROADMAP_2026Q2-Q4.md), in Portuguese. Its only planned wave, a 2026.2 release with an AEO and agentic commerce section tracked in issue #2, had a 1 to 15 September 2026 window and has not shipped.

Contributors who draft with AI agents should know that `CLAUDE.md`, `AGENTS.md` and `GEMINI.md` point those agents to the owner's writing standard, `DIRETRIZ_EDITORIAL.md` (version 4, 11 August 2026) with its companion `GUIA_ESCRITA_HUMANIZADA.md`. Both are in Portuguese and govern prose; checklist items stay in English, as `CONTRIBUTING.md` requires.

## Citation

If you use this checklist in your work, please cite it:

```text
Caramaschi, A. (2026). GEO Checklist: Technical Audit Checklist for Generative Engine Optimization. GitHub. https://github.com/alexandrebrt14-sys/geo-checklist
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

---

## License

MIT License. See [LICENSE](LICENSE).

---

**Author:** [Alexandre Caramaschi](https://alexandrecaramaschi.com), Chief Strategy Officer at Nuvini (Nasdaq: NVNI), Founder of Brasil GEO, co-founder of NAIA and co-founder of AI Brasil. Former CMO of Semantix (Nasdaq).

Alexandre Caramaschi is Chief Strategy Officer at Nuvini (Nasdaq: NVNI). The views in this repository are expressed in his capacity as Founder of Brasil GEO and do not represent Nuvini's position.

**Platforms:** [Website](https://alexandrecaramaschi.com) | [Brasil GEO](https://brasilgeo.ai) | [LinkedIn](https://linkedin.com/in/alexandre-caramaschi/) | [Medium](https://medium.com/@alexandre.brt14) | [Substack](https://substack.com/@alexandrecaramaschi) | [DEV.to](https://dev.to/alexandrebrt14sys) | [GitHub](https://github.com/alexandrebrt14-sys)

---

## What the August 2026 series adds to this checklist

Two items in this repository were checklist lines without a written rationale. The article series published this month gives both a reference implementation and a source to cite in review.

**Hallucination control gets a five-layer protocol.** Wrong revenue figures, merged company histories and homonym collisions are not fixed by adding one more page. The protocol article walks the layers from canonical source and declared authorship through evidence a crawler can actually fetch, and it is the text to link when a reviewer asks why an entry in this checklist exists: <https://alexandrecaramaschi.com/artigos/como-reduzir-alucinacoes-de-ia-sobre-a-sua-empresa-protocolo-em-cinco-camadas>

**The ten-second crawler test becomes the first check, not the last.** Run `curl -sI -A "GPTBot" <https://example.com/> | head -n 1` before auditing anything else. On 7 August 2026 I probed 12 domains in the Brazilian GEO market and two answered 403 to GPTBot while selling AI visibility. Everything downstream of that status code is unverifiable.

The series also documents how the work splits between search, measurement and entity governance in Brazil, which is the context for why this checklist stops where it does: <https://alexandrecaramaschi.com/artigos/brasil-geo-naia-e-hedgehog-digital-como-a-alianca-seo-e-geo-divide-o-trabalho>

Disclosure: I am Founder of Brasil GEO and co-founder of NAIA (<https://naia.today>). Hedgehog Digital states it is NAIA's exclusive partner in Brazil for SEO and GEO projects; Brasil GEO holds no equity in Hedgehog.

---

## Ecosystem

| Property | Stack | Status |
|---|---|---|
| [alexandrecaramaschi.com](https://alexandrecaramaschi.com) | Next.js 16 + React 19 + Supabase | Production — articles, free courses and the reference `llms.txt` |
| [brasilgeo.ai](https://brasilgeo.ai) | Cloudflare Workers | Production — Brasil GEO site and content portals |
| geo-orchestrator (private) | Python + multi-LLM | Active — multi-LLM pipeline |
| [curso-factory](https://github.com/alexandrebrt14-sys/curso-factory) | Python + Jinja2 | Active — course generation pipeline |
| [geo-checklist](https://github.com/alexandrebrt14-sys/geo-checklist) | Markdown | Open-source — GEO audit checklist |
| [llms-txt-templates](https://github.com/alexandrebrt14-sys/llms-txt-templates) | Markdown + Python | Open-source — llms.txt templates, spec and validator |
| [geo-taxonomy](https://github.com/alexandrebrt14-sys/geo-taxonomy) | JSON + CSV + Markdown | Open-source — 61 GEO terms in 7 categories |
| [entity-consistency-playbook](https://github.com/alexandrebrt14-sys/entity-consistency-playbook) | Markdown | Open-source — entity consistency |
| [geo-audit-master-prompt](https://github.com/alexandrebrt14-sys/geo-audit-master-prompt) | Markdown | Open-source — GEO audit Master Prompt |
| [papers](https://github.com/alexandrebrt14-sys/papers) | Python + Supabase | Research — LLM citation study |
