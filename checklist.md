# GEO Audit Checklist

A comprehensive, actionable checklist for auditing and optimizing a website's visibility in generative AI engines.

**How to use:** Work through each section in order. P0 items should be addressed first, P1 second, P2 third. Check off items as you complete them.

---

## 1. Schema Markup

Structured data is the foundation of entity understanding. Without it, LLMs rely on unstructured text extraction, which is unreliable.

- [ ] **P0** — Organization schema is present on the homepage with name, url, logo, description, sameAs, and contactPoint
- [ ] **P0** — sameAs array includes all authoritative profiles: LinkedIn, Crunchbase, Wikipedia/Wikidata, social media, industry directories
- [ ] **P0** — Person schema is implemented for key individuals with name, jobTitle, worksFor, sameAs, knowsAbout
- [ ] **P1** — WebSite schema with SearchAction is present
- [ ] **P1** — Every page has appropriate schema type: Article, Product, Service, FAQPage, HowTo, SoftwareApplication
- [ ] **P1** — Article schema includes author, datePublished, dateModified, publisher, headline, description
- [ ] **P1** — BreadcrumbList schema is present on all interior pages
- [ ] **P1** — Product/Service schema includes name, description, brand, offers, review, aggregateRating
- [ ] **P2** — FAQPage schema is used on pages with question-answer content
- [ ] **P2** — HowTo schema is used on tutorial and guide pages
- [ ] **P2** — speakable property is added to key content sections
- [ ] **P2** — Schema validation passes with zero errors

**Verification:** Use Google Rich Results Test, Schema.org Validator, and inspect raw JSON-LD in page source.

---

## 2. llms.txt

The llms.txt file is a proposed standard that provides LLMs with structured information about a website.

- [ ] **P0** — llms.txt file exists at the domain root
- [ ] **P0** — File contains accurate entity name, description, and key facts
- [ ] **P0** — File includes links to the most important pages with descriptions
- [ ] **P1** — llms-full.txt exists with comprehensive information
- [ ] **P1** — Content is factual, third-person, and free of marketing superlatives
- [ ] **P2** — File is referenced in robots.txt or sitemap for discoverability

---

## 3. Entity Consistency

Entity consistency means every mention of your brand across the internet uses the same name, description, and attributes.

- [ ] **P0** — Primary entity name is identical across all platforms
- [ ] **P0** — Entity description (1-2 sentences) is consistent across all platforms
- [ ] **P0** — Key attributes (founding year, location, industry) are consistent
- [ ] **P1** — Wikipedia/Wikidata entry exists and is accurate
- [ ] **P1** — Crunchbase profile is complete and current
- [ ] **P1** — Google Knowledge Panel is claimed and verified
- [ ] **P1** — LinkedIn profiles are complete with consistent entity references
- [ ] **P2** — Industry directories use the canonical entity name
- [ ] **P2** — Press releases use the canonical entity description
- [ ] **P2** — Internal references within your own site are consistent

---

## 4. Citation Signals

Citation signals are content patterns that make it more likely for an LLM to cite your content.

- [ ] **P0** — Content provides direct, definitive answers to specific questions
- [ ] **P0** — Key claims include supporting data: numbers, percentages, dates, named sources
- [ ] **P0** — Content uses clear, extractable sentence structures
- [ ] **P1** — Original research, data, or frameworks are published and clearly attributed
- [ ] **P1** — Content includes properly formatted lists, tables, and structured comparisons
- [ ] **P1** — Author bylines with credentials are present on all content
- [ ] **P2** — Content is cited by other authoritative sources
- [ ] **P2** — Publication dates are visible and content is regularly updated

---

## 5. Multi-Platform Presence

Being present across multiple authoritative platforms increases AI visibility.

- [ ] **P0** — Website has substantial, indexable content
- [ ] **P0** — LinkedIn profiles (company + key people) are complete
- [ ] **P1** — Content is published on 2-3 third-party platforms
- [ ] **P1** — GitHub presence exists with relevant resources
- [ ] **P1** — YouTube or podcast content exists with transcripts
- [ ] **P2** — Conference talks or interviews are published with transcripts
- [ ] **P2** — Industry forum contributions exist

---

## 6. Content Structure

How content is structured affects whether LLMs can extract useful information.

- [ ] **P0** — Pages have clear H1 > H2 > H3 hierarchy
- [ ] **P0** — Key definitions appear in the first 1-2 paragraphs
- [ ] **P0** — Content answers specific questions
- [ ] **P1** — Tables are used for structured comparisons
- [ ] **P1** — Lists are used for multi-item information
- [ ] **P1** — Content avoids excessive JavaScript rendering
- [ ] **P1** — Internal linking creates clear topical clusters
- [ ] **P2** — Glossary or definitions page exists
- [ ] **P2** — Content includes "Last updated" dates

---

## 7. Monitoring

GEO is not a one-time project. AI responses change as models are updated.

- [ ] **P0** — Define 10-20 key queries that your entity should appear in
- [ ] **P0** — Monthly: run queries across ChatGPT, Gemini, Perplexity, and Copilot
- [ ] **P1** — Track citation accuracy
- [ ] **P1** — Track citation frequency over time
- [ ] **P2** — Monitor competitor entities with the same queries
- [ ] **P2** — Document changes after each model update

---

## Summary Scorecard

| Domain | P0 Items | P1 Items | P2 Items | Total |
|---|---|---|---|---|
| Schema Markup | 3 | 5 | 4 | 12 |
| llms.txt | 3 | 2 | 1 | 6 |
| Entity Consistency | 3 | 4 | 3 | 10 |
| Citation Signals | 3 | 3 | 2 | 8 |
| Multi-Platform Presence | 2 | 3 | 2 | 7 |
| Content Structure | 3 | 4 | 2 | 9 |
| Monitoring | 2 | 2 | 2 | 6 |
| **Total** | **19** | **23** | **16** | **58** |

---

*Maintained by [Alexandre Caramaschi](https://alexandrecaramaschi.com) — CEO at Brasil GEO.*
