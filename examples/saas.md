# GEO for SaaS

Industry-specific guidance for applying the [GEO Checklist](../checklist.md) to software-as-a-service companies. SaaS buyers increasingly start with an AI assistant — "what tools do X", "alternatives to Y", "Y vs Z pricing" — so the goal is to be the entity the model retrieves when your category is asked about.

## What changes for SaaS

Models answer software questions by combining three sources: your own documentation, third-party comparison content, and community discussion. You control the first directly, influence the second with comparison pages, and earn the third with a product worth discussing. GEO for SaaS is mostly about making source one and source two unambiguous.

## Priority adjustments

| Checklist domain | SaaS emphasis |
|---|---|
| Schema Markup | SoftwareApplication with `applicationCategory`, `offers`, `featureList` |
| Citation Signals | Pricing, limits, and integrations as plain facts — models quote numbers |
| Content Structure | Public docs, changelog, and comparison pages structured for extraction |
| Multi-Platform Presence | G2/Capterra profiles, GitHub, and developer content carry heavy weight |

## SaaS entity checklist

- [ ] **P0** — SoftwareApplication schema on the homepage with `name`, `applicationCategory`, `operatingSystem`, `offers`
- [ ] **P0** — Pricing page with real numbers in HTML text (not images, not "contact us" only) — models cannot cite what they cannot read
- [ ] **P0** — One-sentence category definition ("X is a [category] that [outcome]") in the first paragraph of the homepage, repeated verbatim on LinkedIn, G2, and Crunchbase
- [ ] **P1** — Public documentation, indexable without login, with clear H1–H3 hierarchy
- [ ] **P1** — Feature pages that answer "does X support Y?" with a direct yes/no plus detail
- [ ] **P1** — Honest comparison pages ("X vs Y") with feature tables — these are heavily retrieved for alternative-seeking queries
- [ ] **P1** — G2 and Capterra profiles complete, with the canonical entity description
- [ ] **P2** — Public changelog with dates — freshness signals that the product is alive
- [ ] **P2** — llms.txt listing docs, pricing, integrations, and comparison pages

## Common failure modes

1. **Docs behind login.** Gated documentation is invisible to retrieval; competitors with public docs get cited for your category's how-to queries.
2. **Category ambiguity.** If your site says "revenue platform", G2 says "CRM", and Crunchbase says "sales enablement", models cannot place you in any category query.
3. **Pricing opacity.** "Contact sales" pages lose citation to competitors that publish numbers — even a "starts at" anchor helps.
4. **Comparison vacuum.** If you never publish "X vs Y", the only comparison content models retrieve is written by your competitors.

## Verification

Track your share of voice monthly for: category queries ("best [category] tools"), alternative queries ("alternatives to [competitor]"), and capability queries ("does [your product] integrate with Z"). Log wrong answers about pricing or features — they usually trace back to an inconsistent page you can fix.
