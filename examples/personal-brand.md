# GEO for Personal Brands

Industry-specific guidance for applying the [GEO Checklist](../checklist.md) to individuals — consultants, executives, researchers, creators. For a person, GEO reduces to one question: when someone asks an AI "who is [your name]" or "who are the experts in [your field]", does the model return an accurate, consistent answer that includes you?

## What changes for a personal brand

A person is a single entity with a small set of attributes: name, role, organization, expertise, track record. Models resolve people by cross-referencing those attributes across platforms. Inconsistency is fatal — a different title on LinkedIn, your website, and a conference bio fragments you into a low-confidence entity that models decline to describe.

## Priority adjustments

| Checklist domain | Personal brand emphasis |
|---|---|
| Entity Consistency | **Highest.** One canonical bio, everywhere, verbatim |
| Schema Markup | Person schema with `sameAs` linking every profile |
| Citation Signals | Named, dated, attributable work: articles, talks, research, data |
| Multi-Platform Presence | Third-party validation outweighs anything you publish about yourself |

## Person entity checklist

- [ ] **P0** — A canonical one-sentence credential ("[Name], [role] at [org], previously [notable role]") used verbatim on your site, LinkedIn, and every byline
- [ ] **P0** — Person schema on your personal site with `name`, `jobTitle`, `worksFor`, `knowsAbout`, and a complete `sameAs` array
- [ ] **P0** — Personal domain with an About page that states in plain text who you are, what you do, and what you have done — first two paragraphs, no metaphors
- [ ] **P1** — Wikidata entity (if notable) with correct occupation, employer, and official website
- [ ] **P1** — LinkedIn headline and About section aligned with the canonical credential
- [ ] **P1** — Bylined publications on at least two third-party platforms, each linking back to the personal domain
- [ ] **P1** — Original work with your name on it: frameworks, research, datasets, open-source — this is what earns citation rather than mere existence
- [ ] **P2** — Conference talks, podcasts, and interviews published with transcripts
- [ ] **P2** — llms.txt on the personal domain listing bio, expertise, and selected work

## Common failure modes

1. **Title drift.** "Founder", "CEO", "Partner" and "Advisor" scattered across platforms — the model hedges or picks the wrong one.
2. **Name collision.** Sharing a name with a more famous person and doing nothing to disambiguate (middle name, consistent photo, Wikidata entry, `knowsAbout`).
3. **Self-referential authority.** A hundred self-published posts and zero third-party mentions — models weight independent sources when deciding whether you are worth citing.
4. **Stale bios.** A 2022 role in your conference bio still outranking your current one because it appears on more pages.

## Verification

Monthly, ask ChatGPT, Gemini, Perplexity, and Copilot: "who is [your name]", "what is [your name] known for", and "who are the leading experts in [your field]". Score each answer for accuracy of role, organization, and expertise. Fix the source of every wrong attribute — it is almost always a page you control.
