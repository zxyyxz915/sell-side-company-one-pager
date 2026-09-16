---
name: sell-side-company-one-pager
description: Create, update, or audit a sell-side company one-pager and its supporting knowledge base, centered on current operations, product-level volume-price-cost-profit decomposition, income-statement bridges, and consensus forecasts. Use for company cards, earnings trackers, one-page company summaries, or source collection intended to maintain them; do not use for full initiation reports, valuation reports, industry-chain reports, or generic company profiles.
---

# Sell-Side Company One-Pager

Build a dynamic earnings-tracking card, not a company encyclopedia. The required reasoning chain is:

`effective capacity -> output -> sales volume -> realized/assumed price -> revenue -> unit cost -> gross profit -> attributable net profit -> full-year forecast`

## Load the relevant rules

- For creating, updating, or auditing the deliverable, read [references/one-pager-schema.md](references/one-pager-schema.md).
- For collecting materials, building the knowledge base, deciding freshness, or reconciling sources, also read [references/data-and-update-rules.md](references/data-and-update-rules.md).

## Non-negotiable requirements

1. Set and display an as-of date `T`. Never call information "latest" without a publication date and covered period.
2. Put current operations and earnings drivers before static company background.
3. Separate company-disclosed data, standardized database data, analyst calculations, and broker forecasts. Never blend them into one unlabeled figure.
4. Distinguish historical, current effective, ramping, under-construction, and planned capacity. Do not double count replacement, expansion, or already-completed projects.
5. Reconcile every material product through volume, price, cost, and profit. Do not present a revenue or profit forecast without its core assumptions.
6. Use the latest relevant operating price, not a stale historical trough or an arbitrary spot quote. State whether the price is realized, market, or forecast.
7. Compare the latest disclosure with the previous disclosed or modeled value and state what changed.
8. Treat consensus as a benchmark, not truth. Check whether its timestamp postdates the latest results and whether its assumptions reflect new operating information.
9. When a material number cannot be verified, label it `待核验` and show the missing source or assumption. Do not fill gaps with unsupported inference.
10. Preserve all decision-useful source material in the knowledge base even if only the most material items appear on the one-pager.

## Exclusions

Unless the user explicitly changes scope, exclude:

- valuation multiples, target prices, ratings, and upside;
- long/short investment logic;
- industry-chain surveys or long competitive-landscape sections;
- risk-factor boilerplate;
- catalyst calendars;
- management biographies, corporate history, and detailed ownership chains;
- research-question outlines and generic product-use descriptions.

Project commissioning dates may still appear under current operations when they directly affect production or earnings; present them as verified operating status, not a catalyst calendar.

## Working method

1. Inventory the available documents and identify the newest official financial report, operating disclosure, results briefing, and forecast snapshot.
2. Build a six-month operating timeline from all material announcements and valid meeting notes. Do not arbitrarily cap the number of notes collected.
3. Create the current capacity and project-status ledger, resolving conflicts before modeling earnings.
4. Build product-level volume-price-cost-profit estimates and reconcile them to the reported income statement.
5. Bridge period-on-period net-profit changes into volume, price, cost, expenses, non-recurring items, tax, and minority interests where evidence permits.
6. Produce the full-year forecast and compare it with Wind or an equivalent consensus source. Explain material gaps through assumptions.
7. Render only the information needed for rapid analyst review; keep detailed evidence and calculations in the knowledge base or supporting workbook.
8. Run the acceptance checks in the schema before delivery. If a blocking check fails, deliver a data-gap list instead of a falsely complete one-pager.

## Evidence labels

Use these labels consistently:

- `A` — company filing, exchange disclosure, official presentation, or official meeting record;
- `B` — Wind or another standardized/industry database;
- `C` — analyst calculation derived from stated inputs;
- `D` — broker or consensus forecast.

For each material figure retain: source name, publication date, covered period, evidence label, unit, and extraction or calculation note.
