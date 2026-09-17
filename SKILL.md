---
name: sell-side-company-one-pager
description: Create, update, or audit a sell-side company one-pager and its supporting knowledge base, focused on explaining current earnings changes through business drivers and an income-statement bridge. Use for company cards, earnings trackers, one-page company summaries, and their source collection; do not use for generic company profiles, full initiation reports, valuation reports, or industry-chain reports.
---

# Sell-Side Company One-Pager

Produce an earnings explanation, not a classified data inventory. The page must answer:

1. What changed in the latest reporting period?
2. Where in the income statement did profit change?
3. Which business drivers caused it?
4. What evidence supports the explanation, and what remains undisclosed?
5. What should be watched next?

## Load the relevant rules

- For creating, updating, or auditing the one-pager, read [references/one-pager-schema.md](references/one-pager-schema.md).
- For searching ima knowledge-base files, iFinD, 知识星球, 巨潮资讯网, exchange filings, company materials, or other sources, also read [references/data-and-update-rules.md](references/data-and-update-rules.md).

## What counts as a real split

Distinguish three levels:

- **Business split:** identifies which product or segment contributed revenue, gross profit, or profit.
- **Driver split:** explains the change through volume, price, cost, mix, utilization, or project status.
- **Income-statement split:** reconciles gross-profit change, expenses, other gains/losses, tax, minority interests, and attributable net profit.

Listing product revenues or sorting facts into categories is not, by itself, an earnings split. If business-level cost or volume is undisclosed, do not pretend the split is complete. State the boundary once, then complete the strongest supported driver and income-statement analysis.

## Non-negotiable requirements

1. Set and display an as-of date `T`; retain publication date and covered period for every material item.
2. Lead with the latest earnings conclusion. Static background must not occupy material page space.
3. Every visible row must help answer at least one of: `what changed`, `by how much`, `why`, or `what it means for earnings`. Delete rows that do none of these.
4. Separate company-disclosed actuals, standardized database data, analyst calculations, market/industry indicators, third-party notes, and broker forecasts.
5. Do not label an industry or spot-market price as the company's realized price. Do not infer product profit from unmatched market prices, company revenue, or consolidated cost.
6. Build a numerical income-statement bridge before adding peripheral operating details. Reconcile the bridge to the reported change in profit.
7. Use product-level volume-price-cost-profit calculations only when the inputs are traceable, definition-matched, and period-matched.
8. When important product data is unavailable, remove unsupported columns instead of displaying a wide empty table. Add one concise disclosure-boundary note outside the table.
9. Treat consensus as an optional benchmark, not the analytical core. Never include ratings, target prices, valuation multiples, or upside unless explicitly requested.
10. Preserve detailed source inventories, capacity ledgers, price histories, database diagnostics, and missing-data logs in the knowledge base or working papers, not on the main page unless they directly explain current earnings.

## Data-integrity red lines

These override completeness and presentation goals:

- No source, no number. An unsupported output stays empty or the unsupported column is omitted.
- Empty is not zero. Enter `0` only when a traceable same-period source explicitly reports zero.
- Never invent, interpolate, eyeball, or silently proxy missing company data.
- A derived value is allowed only when every input is traceable, definition-matched, period-matched, and the formula is retained.
- Do not convert a disclosed range to a midpoint unless the user explicitly requests that convention.
- Do not back-solve product cost, gross profit, or realized price from consolidated totals unless all residual components are complete and compatible.
- Never use a period minimum, one-day low, stale trough, or preferred outcome as a base price.
- Scenario estimates, when explicitly requested, must sit outside actual-data tables and show assumptions and ranges.

## Default analytical order

1. Identify the latest official financial and operating disclosures and compare them with the prior-year period and previous quarter.
2. Quantify the profit change from gross profit through attributable net profit.
3. Explain the gross-profit change using the narrowest supported business and driver evidence.
4. Identify the latest quarter's inflection: revenue growth, cost change, margin change, and profit change.
5. Add only the operating developments and forward indicators that can alter the earnings path.
6. Add consensus or named broker forecasts only if they improve understanding of forward earnings expectations.
7. Cut everything that merely demonstrates data collection or repeats the same conclusion.

## Exclusions

Unless explicitly requested, exclude:

- valuation multiples, target prices, ratings, upside, and shareholder-count statistics;
- long/short investment logic, generic risks, and catalyst calendars;
- long industry-chain, product-use, corporate-history, management, or ownership descriptions;
- database field diagnostics, connector limitations, price-gate mechanics, and long missing-data appendices;
- detailed capacity tables, price histories, or meeting-note inventories that do not explain the latest earnings change.

## Evidence labels

- `A` — formal company filing, exchange disclosure, company presentation, or official meeting record;
- `B` — iFinD, Wind, or another standardized/licensed database;
- `C` — analyst calculation derived from stated inputs;
- `D` — named broker or consensus forecast;
- `E` — traceable third-party meeting note or industry data.

ima is a storage and retrieval layer, not an evidence grade. Grade an ima document according to its underlying original source. 知识星球 content is normally `E` unless it reproduces a traceable higher-ranked original.
