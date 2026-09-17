# Data, Source, and Update Rules

## 1. Establish the cut-off

Set `T` as the knowledge-base and one-pager cut-off. For every item retain:

- company name and ticker;
- source and original link or file;
- publication date;
- covered period;
- data unit and currency;
- evidence label `A/B/C/D/E`;
- source type and, for ima or reposted material, the underlying original source;
- affected one-pager field;
- whether the item supersedes an earlier value.

Reject or quarantine material with no identifiable source, publication date, or covered period.

### Missing-data rule

- If no qualified source exists, leave the corresponding output cell empty.
- Do not use `0`, `—`, `N/A`, a guessed value, or prose such as `待核验` inside a numeric cell as a substitute for data. Omit broadly unavailable columns from the one-pager and record the detailed gap in working papers.
- Zero is valid only when a traceable source explicitly reports zero for the same company, field, and period.
- Do not infer a missing number from peers, industry averages, anonymous notes, partial screenshots, or visual estimation from a chart.
- Do not back-solve a missing product value from consolidated data unless the remaining components are complete, definition-matched, and the residual formula is explicitly shown. Otherwise leave it empty.
- A broker estimate may populate only a clearly labeled broker/consensus column. It must not fill a company-actual or analyst-derived field.

## 2. Permitted sources and retrieval rules

Use any connected or user-provided source that improves coverage, including ima knowledge bases, iFinD, 知识星球, 巨潮资讯网, stock-exchange websites, company investor-relations pages, broker reports, and traceable industry databases. Availability does not make sources equally authoritative.

### ima knowledge base

- Search the target-company folder and aliases for financial reports, operating announcements, presentations, meeting notes, broker reports, price data, and project updates.
- Treat ima as a document container and retrieval layer. Determine the evidence grade from the document's original issuer, not from ima.
- Prefer the original PDF or captured original link. Retain title, issuer, publication date, covered period, and ima file identifier/path.
- Deduplicate copies stored under different names. Repeated copies are not independent confirmation.

### 巨潮资讯网, stock exchanges, and company IR

- Use 巨潮资讯网, 上交所/深交所/北交所, and company IR pages for original filings and announcements.
- These are the default sources for reported actuals, project status, guidance, and corrections.
- Search both the formal financial report and separate operating-data announcements; one may contain business revenue while the other contains the consolidated cost base.
- If a portal mirror is easier to retrieve, verify title, ticker, date, and text against the official disclosure before grading it `A`.

### iFinD and Wind

- Use iFinD or Wind for standardized statements, single-quarter data, business composition, market/industry series, consensus, and named-broker forecasts.
- Record the terminal field or table name, reporting period, extraction date, unit, and whether the value is reported, standardized, or estimated.
- A blank standardized field does not prove that the company never disclosed the item; check the original filing and notes.
- A populated field does not automatically prove a same-period company disclosure. Trace material product costs, margins, and realized prices back to the original source before treating them as actuals.

### 知识星球 and third-party meeting notes

- Search all relevant notes from the previous six months, plus older notes still needed to understand a live project or guidance change.
- Retain author/institution, event type, event date, publication date, and management participants when available.
- Use a note as evidence only when the event and date are traceable. Anonymous screenshots, unattributed excerpts, and reposts without an original event are leads, not facts.
- A traceable management statement may explain direction, timing, or guidance, but does not override a later formal filing.
- Do not convert qualitative comments such as `prices improved`, `orders were strong`, or `costs declined` into numerical actuals.

### Other portals, news, and industry data

- Use 东方财富, 同花顺资讯, 新浪财经, 雪球公告镜像, and news reports mainly for discovery or fallback access to an original document.
- Use traceable industry sources for prices, utilization, inventory, and input costs; label them as market/industry indicators, never as company realized data.
- Search snippets, AI summaries, and undated reposts cannot support a material number.

### Retrieval order

1. Newest official financial report and notes.
2. Separate operating announcements, guidance, and corrections.
3. Official results presentations and meeting records.
4. ima archive for missing company documents, broker reports, and notes.
5. iFinD/Wind standardized data and consensus.
6. 知识星球 and traceable third-party notes.
7. Industry databases and financial portals for remaining indicators or discovery.

Do not stop after the first source merely because it contains many numbers. Cross-check the fields that determine the earnings conclusion.

## 3. Minimum baseline package per company

### Official filings and presentations

- latest three complete annual reports;
- latest two half-year reports where available;
- latest four quarterly reports;
- all results forecasts, preliminary results, and corrections since the latest formal report;
- all material operating announcements from the previous 12 months;
- current projects: retain initial announcement, material changes, commissioning, and latest status even if older than 12 months;
- latest four quarterly/half-year results presentations or official meeting records where available.

Official exchange/company documents outrank all secondary sources.

### Meeting notes and management communication

- collect every valid operating or earnings-related note from the previous six months;
- do not impose a fixed maximum count at ingestion;
- retain notes that contain production, sales, price, cost, orders, inventory, utilization, project progress, or guidance;
- quarantine anonymous excerpts or screenshots that cannot be tied to an institution, date, and event;
- deduplicate repeated reposts but preserve the earliest traceable original.

### Financial and forecast data

Use iFinD, Wind, or an equivalent licensed structured database for:

- three annual periods and eight single quarters of standardized financials;
- reportable-segment or product composition where available;
- current-year and next-two-year consensus revenue, attributable net profit, and EPS;
- contributor count and 30-/90-day forecast changes;
- individual broker forecasts and publication dates when needed for reconciliation.

Direct terminal-to-agent integration is not required. A controlled workflow may export three versioned workbooks into the knowledge base:

1. `company_historical_financials_quarters.xlsx`
2. `company_business_mix_operating_metrics.xlsx`
3. `company_consensus_broker_forecasts.xlsx`

Record the export date. Refresh financials after results; refresh consensus weekly and after material disclosures.

### Industry and product data

For material products only, obtain:

- 24 months of product and key input prices at daily or weekly frequency;
- 12 months of utilization, inventory, or spread data where decision-useful;
- latest transaction/realized-price evidence from the company when available.

Use licensed or traceable sources such as iFinD, Wind, Baiinfo, OilChem, exchange data, government statistics, or company disclosure. Do not use an undated web snippet as a model input.

## 4. Source hierarchy

Resolve conflicts in this order, while considering covered period and definitions:

1. formal company filing or exchange announcement;
2. official results presentation or official meeting record;
3. government or exchange statistics;
4. iFinD, Wind, or another standardized licensed database;
5. traceable industry database;
6. broker report with named analyst and date;
7. traceable third-party meeting note;
8. financial portal or news report;
9. anonymous repost or unverified excerpt.

A lower-ranked source may be more current, but it must not silently overwrite a higher-ranked figure. Show both in working papers, explain the period/definition difference, and choose a modeling input explicitly. On the one-pager, show only the value needed for the earnings explanation.

ima has no fixed rank. Use the rank of the underlying document: a company announcement stored in ima remains level 1; an anonymous note stored in ima remains unverified.

## 5. Freshness rules

| Data type | Baseline window | Refresh trigger |
|---|---|---|
| Announcements | Previous 12 months plus still-live projects | Daily |
| Results briefings and official IR | Previous four reporting events | On publication |
| Third-party meeting notes | All valid notes from previous six months | Daily |
| Product/input prices | 24-month history plus latest week | Weekly or after material move |
| Utilization/inventory/spreads | Previous 12 months | Weekly |
| Standardized financials | Three years and eight single quarters | After each results release |
| Consensus forecasts | FY0–FY2 with contributor count | Weekly and after results/material disclosure |
| Capacity/project ledger | Full history for live projects | On any status change |

Do not use a forecast published before the latest material disclosure without an explicit stale-data warning.

## 6. Reconciliation rules

### Capacity

- Maintain a project identity key to prevent renamed projects from being counted twice.
- Record original capacity, incremental capacity, replacement capacity, commissioning date, and ramp status separately.
- Cross-check the current total against the latest company statement.

### Price

- Label each price as realized, list, spot, contract, market average, or model assumption.
- Record product grade/specification, geography, tax basis, freight basis, currency, unit, observation frequency, and start/end dates. A price with an unknown definition is ineligible for profit calculation.
- Match the price period to the volume period. Do not substitute a current spot price for a historical realized price without a bridge.
- For an actual historical period, use the company-disclosed realized price for the same product and period. If it is not disclosed, derive `product revenue / product sales volume` only when both inputs come from qualified, definition-matched disclosures for the same period. Otherwise leave the realized-price cell empty.
- A price appearing in an `industry conditions`, `market review`, or similar section of a company report remains an industry/market price unless the text explicitly identifies it as the company's transaction or realized price.
- For a current full-year estimate, combine year-to-date realized price with a qualified remaining-period base price using sales-volume weights. Do not apply a current spot quote to the entire year.
- Select the remaining-period base price in this order: (1) current company guidance or traceable contract/settlement price; (2) a traceable benchmark average for the exact product definition; otherwise leave it empty.
- When using a benchmark fallback, calculate both the latest 30-calendar-day average and 90-calendar-day average, each ending no more than 7 calendar days before `T`. For weekly data, use the latest 4-week and 13-week averages, with the final observation no more than 14 days before `T`.
- Use the short-window average as the base only when it differs from the long-window average and the latest company-realized comparable price by no more than 15%. If either deviation exceeds 15%, stop automatic calculation, leave the forecast-price cell empty, and request human selection with the competing values shown.
- Never use a period minimum, period maximum, one-day low/high, or an old cyclical trough as the base case. Do not select a quote because it produces a preferred profit result.
- If the company discloses only a price range, retain the range. Do not silently take its midpoint, lower bound, or upper bound.
- Verify the implied price `revenue / sales volume` against the selected price. A discrepancy above 5% requires a definition/period reconciliation before use.

### Cost

- Distinguish cash cost, production cost, cost of sales, freight-inclusive cost, and full cost.
- Do not compare differently defined costs as if they were the same.
- Use a company-disclosed same-product, same-period unit cost where available. Derive unit cost only from matched product cost of sales and product sales volume.
- Do not divide consolidated cost of sales by one product's volume or use a peer's unit cost as the company's cost.
- For a current forecast, carry forward the latest qualified unit cost only when its definition is unchanged and no material input-cost or operating-status change has occurred. Otherwise update it through traceable inputs and an explicit formula, or leave it empty.
- If the source provides only a cost range, preserve the range; do not select the lower bound to maximize profit or the upper bound to minimize profit.

### Calculation eligibility gate

Before calculating product revenue or profit, all material inputs must pass:

| Check | Required condition |
|---|---|
| Identity | Exact company, product/segment, and project |
| Period | Volume, price, and cost cover compatible periods |
| Definition | Grade, geography, tax, freight, currency, and unit are known and compatible |
| Freshness | Forecast inputs meet the price/cost freshness rules |
| Provenance | Each input has a traceable source and publication/observation date |
| Status | Actual, derived, analyst assumption, and broker forecast are clearly separated |
| Outlier | Price guards and implied-price reconciliation pass |

If any material check fails, leave that calculation and all dependent cells empty. If most rows would be empty, omit the affected columns from the one-pager, state the disclosure boundary once, and record the detailed failure in the working-paper data-gap log. Do not repair it with an unsupported assumption.

### Financial statements

- Preserve reported cumulative figures before deriving single quarters.
- Check units, currency, restatements, consolidation scope, acquisitions, disposals, and minority interests.
- Reconcile product/segment gross profit with consolidated gross profit; explain residuals such as intersegment elimination or undisclosed businesses.

### Forecasts

- Extract the forecast date and underlying period.
- Rebuild material revenue and gross-profit assumptions from volume, price, and cost.
- Compare analyst model, consensus, and major broker range.
- Explain differences; never average incompatible assumptions mechanically.

## 7. Incremental update behavior

When a new document arrives:

1. identify company, document type, publication date, and covered period;
2. link it to the affected fields;
3. compare extracted values with current stored values;
4. classify each change as new, confirmed, revised, superseded, or conflicting;
5. update the capacity/project ledger and earnings assumptions before rewriting narrative;
6. re-run the eligibility gate and recalculate revenue, gross profit, and net profit only if all material volume, price, cost, tax, minority-interest, and consolidation inputs qualify;
7. record an update log with old value, new value, reason, source, and model impact;
8. flag for human review when conflict or earnings impact is material.

Do not append every new document to the visible one-pager. Update the affected field and preserve the underlying evidence in the knowledge base.
