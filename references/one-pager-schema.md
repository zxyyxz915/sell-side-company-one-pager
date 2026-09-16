# One-Pager Schema and Acceptance Rules

## Contents

1. Page structure
2. Required tables
3. Calculation rules
4. Presentation constraints
5. Blocking acceptance checks

## 1. Page structure

The main page has five blocks. A block may be shortened only when the company genuinely lacks the relevant business structure, not to hide missing data.

| Block | Purpose | Target share |
|---|---|---:|
| Header and company snapshot | Identify the company, earnings engine, and data cut-off | 5%–10% |
| Latest operations | Show what changed since the prior disclosure | 20% |
| Product/business earnings split | Explain volume, price, cost, and gross profit | 30% |
| Income-statement bridge | Reconcile gross profit to attributable net profit | 25% |
| Forecast and consensus comparison | Show forecast assumptions and market benchmark | 15%–20% |

### Header and company snapshot

Include only:

- company name and ticker;
- one-sentence earnings model;
- core products or reportable segments;
- latest financial reporting period;
- operating-data cut-off and page update date.

Do not create a standalone multi-section company profile. Production locations belong here only if location materially changes costs or operating risk.

### Latest operations

Show the three to five most material changes on the page, while retaining all valid six-month items in the knowledge base.

| Date | Item | Previous state/value | Current state/value | Earnings implication | Source |
|---|---|---|---|---|---|

Cover, when material:

- production, sales volume, utilization, inventory, or orders;
- realized or market prices and key input costs;
- commissioning, ramp-up, maintenance, shutdown, or restart;
- acquisition/disposal integration and consolidation timing;
- revised management guidance.

Maintain a capacity ledger:

| Product | Historical capacity | Current effective capacity | Ramping | Under construction | Planned | Expected contribution period | Source |
|---|---:|---:|---:|---:|---:|---|---|

Count a project as effective capacity only after evidence of commissioning or commercial production. Record ramping capacity separately until stable production is supported.

### Product/business earnings split

Use the narrowest economically meaningful unit supported by evidence: product, segment, mine, plant, or geography.

| Product/segment | Effective capacity | Output | Sales volume | Realized/assumed price | Unit cost | Unit gross profit | Revenue | Gross profit | Gross margin | Evidence |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|

For each row distinguish actual, implied, and forecast values. If quarterly segment disclosure is unavailable, use the latest official half-year or annual split and do not fabricate quarterly detail.

### Income-statement bridge

| Item | Prior-year period | Previous quarter | Current period | YoY | QoQ | Main driver | Evidence |
|---|---:|---:|---:|---:|---:|---|---|
| Revenue | | | | | | | |
| Cost of goods sold | | | | | | | |
| Gross profit | | | | | | | |
| Gross margin | | | | | | | |
| Selling expense | | | | | | | |
| Administrative expense | | | | | | | |
| R&D expense | | | | | | | |
| Finance expense | | | | | | | |
| Investment income | | | | | | | |
| Other income | | | | | | | |
| Impairment | | | | | | | |
| Income tax | | | | | | | |
| Minority interests | | | | | | | |
| Attributable net profit | | | | | | | |
| Recurring attributable net profit | | | | | | | |

Add a compact profit-change bridge when evidence supports it:

| Driver | Estimated profit impact | Direction | Method/source |
|---|---:|---|---|
| Volume | | Positive/negative | |
| Price | | Positive/negative | |
| Unit cost | | Positive/negative | |
| Expenses | | Positive/negative | |
| Non-recurring items | | Positive/negative | |
| Tax and minority interests | | Positive/negative | |

### Forecast and consensus comparison

Forecast the current year and next two years unless the assignment states otherwise.

| Metric | Latest actual | FY0E | FY1E | FY2E |
|---|---:|---:|---:|---:|
| Revenue | | | | |
| Gross profit | | | | |
| Attributable net profit | | | | |
| Recurring attributable net profit | | | | |
| EPS | | | | |

Compare the model with market forecasts:

| Metric | Analyst model | Wind/equivalent consensus | Broker range | Difference | Main assumption causing difference |
|---|---:|---:|---:|---:|---|

Include the consensus extraction date and contributor count. Do not show PE, PB, EV/EBITDA, target price, rating, or upside.

## 2. Calculation rules

Use consistent units and show conversions.

```text
utilization = output / period-effective capacity
sales ratio = sales volume / output
revenue = sales volume × realized or assumed price
unit gross profit = realized or assumed price - unit cost
product gross profit = sales volume × unit gross profit
gross profit = revenue - cost of goods sold
attributable net profit = net profit - minority interests
```

For cumulative filings, calculate single-quarter figures explicitly, for example:

```text
Q3 single-quarter = 9M cumulative - H1 cumulative
Q2 single-quarter = H1 cumulative - Q1
Q4 single-quarter = FY cumulative - 9M cumulative
```

Record the calculation as evidence label `C` and retain both inputs.

When decomposing revenue or profit changes, avoid false precision. Use disclosed quantities and prices where available; otherwise label the result as an estimate and provide a range when input uncertainty is material.

## 3. Required interpretation

The one-pager must explicitly answer:

1. What changed since the previous disclosure?
2. Which product or segment contributes the most revenue and gross profit?
3. Is the earnings change driven mainly by volume, price, cost, expenses, or non-recurring items?
4. What is the current effective capacity rather than merely announced capacity?
5. What operating assumptions support the full-year profit forecast?
6. Why does the forecast differ from consensus or major brokers?

## 4. Presentation constraints

- Prefer four compact tables and no more than three short conclusion sentences.
- Use one unit per column and state whether monetary figures are RMB mn, RMB 100mn, USD mn, or another unit.
- Show YoY and QoQ only where the comparison is economically and seasonally meaningful.
- Move detailed source notes and calculations to the supporting workbook or knowledge base.
- Keep static company background to no more than roughly 10% of the page.
- Do not hide uncertainty in polished prose. Use `待核验`, `公司未披露`, or `分析测算`.

## 5. Blocking acceptance checks

Do not label the deliverable complete if any of the following is true:

- the newest material official results briefing or operating disclosure is absent;
- the six-month material meeting-note timeline is incomplete without explanation;
- effective capacity includes planned or under-construction capacity;
- a material project is double counted or uses superseded status;
- a key price or cost assumption lacks a date, period, or source;
- company-disclosed and analyst-estimated figures are mixed without labels;
- product gross profit does not reconcile plausibly with consolidated gross profit;
- attributable net profit ignores material tax, minority interests, or non-recurring items;
- the forecast is only a copied consensus number with no operating assumptions;
- consensus predates material new results or operating information without warning;
- the page is dominated by excluded background, valuation, risk, or industry-chain content.

If blocked, return a table with `missing/incorrect field`, `current value`, `required evidence`, `preferred source`, and `impact on earnings`.
