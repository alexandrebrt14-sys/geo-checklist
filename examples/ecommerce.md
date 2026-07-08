# GEO for E-commerce

Industry-specific guidance for applying the [GEO Checklist](../checklist.md) to online stores. E-commerce has one structural advantage in GEO: every product is a well-defined entity with a name, a price, and attributes. The work is making that structure machine-readable and consistent everywhere the product appears.

## What changes for e-commerce

When a shopper asks an AI assistant "what is the best running shoe under $150" or "is brand X reliable", the model composes an answer from product entities, reviews, and comparisons it can extract cleanly. Stores that publish structured product data get cited; stores that rely on rendered JavaScript and marketing copy do not.

## Priority adjustments

| Checklist domain | E-commerce emphasis |
|---|---|
| Schema Markup | **Highest.** Product, Offer, AggregateRating, Review on every product page — this is your citation surface |
| Entity Consistency | Brand name and product names identical across store, marketplaces, and review platforms |
| Citation Signals | Specs, dimensions, materials, and prices as extractable facts, not prose |
| Content Structure | Comparison tables and buying guides outrank adjective-heavy category copy |

## Product entity checklist

- [ ] **P0** — Product schema on every product page with `name`, `description`, `brand`, `sku`, `image`
- [ ] **P0** — Offer schema with `price`, `priceCurrency`, `availability` — kept in sync with the actual catalog
- [ ] **P0** — AggregateRating and Review schema populated from real reviews (never fabricated)
- [ ] **P1** — Canonical product names identical on your store, Amazon/marketplaces, Google Shopping, and review sites
- [ ] **P1** — Category pages with a clear definition of the category in the first paragraph
- [ ] **P1** — Buying guides that answer specific questions ("how to choose X") with comparison tables
- [ ] **P2** — FAQPage schema on product pages covering sizing, shipping, returns
- [ ] **P2** — llms.txt listing top categories and best-selling products with one-line descriptions

## Common failure modes

1. **Client-side rendering hides the catalog.** If product data only exists after JavaScript executes, most AI crawlers never see it. Server-render product pages or emit static JSON-LD.
2. **Price drift.** Schema says $99, page says $89 — models learn to distrust the source. Automate schema generation from the catalog.
3. **Marketplace entity split.** "ACME Store", "ACME Official" and "ACME Brasil" read as three different entities. Pick one canonical name.
4. **Review markup without reviews.** Empty or fabricated rating markup is a spam signal for both search engines and LLM retrieval pipelines.

## Verification

Run 10 purchase-intent queries ("best [category] for [use case]") monthly across ChatGPT, Gemini, Perplexity, and Copilot. Track whether your products appear, whether prices are quoted correctly, and which competitor entities are cited instead.
