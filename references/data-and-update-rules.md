# Data, Source, and Update Rules

## 1. Establish the cut-off

Set `T` as the knowledge-base and one-pager cut-off. For every item retain:

- company name and ticker;
- source and original link or file;
- publication date;
- covered period;
- data unit and currency;
- evidence label `A/B/C/D`;
- affected one-pager field;
- whether the item supersedes an earlier value.

Reject or quarantine material with no identifiable source, publication date, or covered period.

## 2. Minimum baseline package per company

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

Prefer Wind or an equivalent licensed structured database for:

- three annual periods and eight single quarters of standardized financials;
- reportable-segment or product composition where available;
- current-year and next-two-year consensus revenue, attributable net profit, and EPS;
- contributor count and 30-/90-day forecast changes;
- individual broker forecasts and publication dates when needed for reconciliation.

Direct Wind-to-agent integration is not required. A controlled workflow may export three versioned workbooks into the knowledge base:

1. `company_historical_financials_quarters.xlsx`
2. `company_business_mix_operating_metrics.xlsx`
3. `company_consensus_broker_forecasts.xlsx`

Record the export date. Refresh financials after results; refresh consensus weekly and after material disclosures.

### Industry and product data

For material products only, obtain:

- 24 months of product and key input prices at daily or weekly frequency;
- 12 months of utilization, inventory, or spread data where decision-useful;
- latest transaction/realized-price evidence from the company when available.

Use licensed or traceable sources such as Wind, Baiinfo, OilChem, exchange data, government statistics, or company disclosure. Do not use an undated web snippet as a model input.

## 3. Source hierarchy

Resolve conflicts in this order, while considering covered period and definitions:

1. formal company filing or exchange announcement;
2. official results presentation or official meeting record;
3. government or exchange statistics;
4. Wind or another standardized licensed database;
5. traceable industry database;
6. broker report with named analyst and date;
7. traceable third-party meeting note;
8. financial portal or news report;
9. anonymous repost or unverified excerpt.

A lower-ranked source may be more current, but it must not silently overwrite a higher-ranked figure. Show both, explain the period/definition difference, and choose a modeling input explicitly.

## 4. Freshness rules

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

## 5. Reconciliation rules

### Capacity

- Maintain a project identity key to prevent renamed projects from being counted twice.
- Record original capacity, incremental capacity, replacement capacity, commissioning date, and ramp status separately.
- Cross-check the current total against the latest company statement.

### Price

- Label each price as realized, list, spot, contract, market average, or model assumption.
- Match the price period to the volume period.
- Do not substitute a current spot price for a historical realized price without a bridge.

### Cost

- Distinguish cash cost, production cost, cost of sales, freight-inclusive cost, and full cost.
- Do not compare differently defined costs as if they were the same.

### Financial statements

- Preserve reported cumulative figures before deriving single quarters.
- Check units, currency, restatements, consolidation scope, acquisitions, disposals, and minority interests.
- Reconcile product/segment gross profit with consolidated gross profit; explain residuals such as intersegment elimination or undisclosed businesses.

### Forecasts

- Extract the forecast date and underlying period.
- Rebuild material revenue and gross-profit assumptions from volume, price, and cost.
- Compare analyst model, consensus, and major broker range.
- Explain differences; never average incompatible assumptions mechanically.

## 6. Incremental update behavior

When a new document arrives:

1. identify company, document type, publication date, and covered period;
2. link it to the affected fields;
3. compare extracted values with current stored values;
4. classify each change as new, confirmed, revised, superseded, or conflicting;
5. update the capacity/project ledger and earnings assumptions before rewriting narrative;
6. recalculate revenue, gross profit, and net profit if a material volume, price, cost, tax, minority-interest, or consolidation assumption changes;
7. record an update log with old value, new value, reason, source, and model impact;
8. flag for human review when conflict or earnings impact is material.

Do not append every new document to the visible one-pager. Update the affected field and preserve the underlying evidence in the knowledge base.
