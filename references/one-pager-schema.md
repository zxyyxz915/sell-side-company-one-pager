# One-Pager Schema and Acceptance Rules

## 1. Outcome standard

The page is successful only if a reader can understand, in under two minutes:

- why the latest revenue and profit changed;
- whether the change came mainly from volume, price, cost, mix, expenses, or non-recurring items;
- whether the latest quarter improved or deteriorated and why;
- which current operating variables can change the next reporting period.

A collection of accurate tables can still fail this standard if it does not connect facts to earnings.

## 2. Default page structure

Use four analytical blocks. Omit a block that has no decision-useful evidence; never fill space for template completeness.

### Block 1 — Core conclusion and latest operating change

Write no more than three conclusion sentences. Together they should cover:

1. the main cause of the latest profit change;
2. the latest-quarter inflection or lack of inflection;
3. the most important forward operating variable.

Then show only three to five material operating changes:

| Date/period | What changed | Previous | Current | Earnings implication | Evidence |
|---|---|---:|---:|---|---|

Include capacity or project status only when it changes production, sales, cost, consolidation scope, or the forecast period. Do not reproduce a full capacity ledger on the page.

### Block 2 — Business and driver split

Use the narrowest company-disclosed business unit. Start with what is actually available.

#### When revenue and gross profit are both disclosed

| Product/segment | Revenue | YoY | Gross profit | Gross margin | Change driver | Evidence |
|---|---:|---:|---:|---:|---|---|

#### When only product/segment revenue is disclosed

| Product/segment | Revenue | YoY | Revenue share | Disclosed operating change | Earnings direction | Evidence |
|---|---:|---:|---:|---|---|---|

Do not add empty columns for sales volume, realized price, unit cost, gross profit, and gross margin. Add one note below the table:

> The company did not disclose same-period product sales volume, realized price, or cost; product-level gross profit cannot be calculated reliably.

If the latest annual report contains a fuller product split, use it only as a compact historical reference. Label the period prominently and do not splice annual cost/margins into the current half-year or quarter.

#### Driver explanation

After the business table, state the supported causal chain:

`volume/project status -> revenue effect; market or realized price -> revenue/margin effect; input cost/utilization -> margin effect; mix -> residual effect`

Quantify each link only when eligible. Otherwise state direction and evidence without manufacturing an amount.

### Block 3 — Income-statement and quarterly bridge

This is mandatory whenever financial statements are available.

#### Profit-change bridge

| Driver | Change or profit impact | Direction | Explanation | Evidence |
|---|---:|---|---|---|
| Gross profit | | | | |
| Selling, administrative, R&D, and finance expenses | | | | |
| Other income, investment income, impairment, and non-operating items | | | | |
| Profit before tax | | | | |
| Tax | | | | |
| Minority interests | | | | |
| Attributable net profit | | | | |

Use signs from the perspective of impact on profit. The bridge must reconcile to the reported attributable-net-profit change, subject only to disclosed rounding.

Do not list every income-statement line when several immaterial lines can be grouped without losing the causal explanation.

#### Latest-quarter inflection

| Metric | Prior-year quarter | Previous quarter | Current quarter | YoY | QoQ | Interpretation |
|---|---:|---:|---:|---:|---:|---|
| Revenue | | | | | | |
| Cost of sales | | | | | | |
| Gross profit | | | | | | |
| Gross margin | | | | | | |
| Attributable net profit | | | | | | |

Derive a single quarter from cumulative reports only with explicit formulas and retained inputs. The interpretation must identify whether the change was driven mainly by revenue or margin; do not claim unit-cost or price improvement without evidence.

### Block 4 — Forward earnings watch

Show only the variables that can materially change the next reporting period:

| Variable | Latest verified state | Direction/change | Earnings channel | Next verification source |
|---|---|---|---|---|

Examples include product prices, key input costs, utilization, orders, inventory, commissioning/ramp-up, shutdowns, or consolidation changes.

Market and industry prices are indicators, not company realized prices. Label them by specification, geography, tax/freight basis, frequency, and observation period.

Consensus is optional:

| Metric | FY0E consensus | Named-broker range | Main disagreement | Extraction date |
|---|---:|---:|---|---|

Do not include rating counts, target prices, or valuation. If no qualified analyst model exists, do not create empty self-forecast columns merely to complete a template.

## 3. Calculation rules

Use consistent units and retain formulas:

```text
gross profit = revenue - cost of sales
gross margin = gross profit / revenue
attributable net profit = net profit - minority interests
Q2 single-quarter = H1 cumulative - Q1 cumulative
Q3 single-quarter = 9M cumulative - H1 cumulative
Q4 single-quarter = FY cumulative - 9M cumulative
```

Product calculations require eligible same-period inputs:

```text
realized price = product revenue / product sales volume
unit cost = product cost of sales / product sales volume
unit gross profit = realized price - unit cost
product gross profit = product revenue - product cost of sales
```

Do not calculate these merely because the formulas are available. Apply the eligibility gate in [data-and-update-rules.md](data-and-update-rules.md).

## 4. Editing test: analysis or clutter

For every table, row, and paragraph ask:

1. Does it quantify an earnings change?
2. Does it explain a cause?
3. Does it identify a forward earnings variable?
4. Is it necessary to understand or verify one of the above?

If all four answers are no, remove it from the page and retain it only in the knowledge base if useful.

Usually remove:

- shareholder counts and ownership percentages;
- ratings and target-price summaries;
- corporate history and generic business descriptions;
- complete project or meeting-note inventories;
- daily price tables with multiple unused averaging windows;
- connector tests, database-field diagnostics, and missing-data mechanics;
- repeated conclusions presented in both tables and prose.

## 5. Disclosure-boundary handling

- Do not display a wide row of empty numeric cells.
- Omit unavailable columns when their absence affects most rows.
- State the disclosure boundary once beneath the relevant table.
- Keep a detailed missing-evidence log in working papers, not on the main page.
- When a requested split is impossible, say which level is complete: for example, `business revenue split complete; product gross-profit and volume-price-cost split unavailable; consolidated profit bridge complete`.

## 6. Blocking acceptance checks

Do not call the page complete if:

- it classifies data but does not reconcile the latest profit change;
- the core conclusion is buried after company background, capacity history, or price tables;
- an industry average or spot quote is described as company realized price;
- current-period product profit is calculated from annual-period costs or mismatched product classifications;
- unsupported product columns are filled, or broad empty tables dominate the page;
- actuals, analyst calculations, market indicators, meeting-note claims, and forecasts are not clearly separated;
- the latest official operating/results material is missing without explanation;
- a material project is double counted or planned capacity is treated as effective;
- the quarterly bridge does not reconcile to cumulative filings;
- the page repeats database search limitations or source-collection process instead of explaining earnings;
- more than roughly 10% of the page is static background;
- excluded valuation, ratings, target prices, generic risks, or catalyst content appears without explicit request.

## 7. Final compression pass

Before delivery:

1. put the profit explanation first;
2. merge immaterial income-statement lines;
3. reduce operating changes to the three to five most consequential;
4. replace long price histories with latest level, comparable-period change, and earnings implication;
5. delete repeated facts and workflow commentary;
6. keep no more than four compact tables plus three conclusion sentences unless the user requests a longer tracker.
