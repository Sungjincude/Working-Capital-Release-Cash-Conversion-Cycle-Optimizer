# Working Capital Release & Cash Conversion Cycle Optimizer

> **Excel financial modelling portfolio project · Corporate finance / turnaround / liquidity**

A driver-based Excel model that quantifies **cash tied up in accounts receivable, inventory and accounts payable**, then estimates the liquidity benefit of improving days sales outstanding (DSO), days inventory outstanding (DIO), and days payable outstanding (DPO).

The example company, **Aster Components Europe**, and all financial inputs are **fictional**. This is a teaching / portfolio model, not company guidance or an implementation forecast.

## Model highlights

- **Two-year baseline (FY2024 and FY2025)** covering revenue, cost of goods sold, receivables, inventory and payables.
- **Working-capital KPI engine:** DSO, DIO, DPO, cash conversion cycle (CCC), and operating net working capital (NWC).
- **Three editable scenario presets:** Conservative, Management and Stretch.
- **Target-setting calculator:** convert days saved into cash released from receivables and inventory, plus the incremental financing from extended supplier terms.
- **Reconciled bridge:** baseline operating NWC → target NWC, by individual driver.
- **Dynamic dashboard and 12 audit controls** for model integrity.

## File

| File | Use |
| --- | --- |
| [Completed Excel model](models/Working_Capital_Release_CCC_Optimizer_Completed.xlsx) | All historical calculations, scenarios, bridge, dashboard and checks |

Download and open the workbook in **Microsoft Excel** to use the dropdowns and formulas. GitHub does not run Excel models inside its browser preview.

## Workbook guide

| Worksheet | Description |
| --- | --- |
| `00_README` | Case description, user instructions, financial definitions, model limitations |
| `01_Historical` | FY2024 / FY2025 inputs, DSO, DIO, DPO, CCC and NWC |
| `02_Targets` | Three editable day-improvement presets and target balance calculations |
| `03_Cash_Bridge` | Stepwise operating NWC reduction and release reconciliation |
| `04_Dashboard` | Scenario dropdown, KPIs, improvement chart and cash-release bridge |
| `05_Audit` | Twelve formula, scenario and reconciliation checks |

## Quick start

1. Open [the workbook](models/Working_Capital_Release_CCC_Optimizer_Completed.xlsx) and go to `04_Dashboard`.
2. Select **Conservative**, **Management** or **Stretch** in the **B6** scenario dropdown.
3. Review actual vs target DSO/DIO/DPO/CCC, the target cash release and supporting charts.
4. Change the **yellow day-driver inputs** in `02_Targets` to test a custom plan.
5. Optionally replace the **blue historical inputs** in `01_Historical` with other illustrative data.
6. Check `05_Audit` — all twelve controls should read **PASS** for the supplied assumptions.

## Financial definitions

Using a **365-day year** and year-end balance proxies:

```text
DSO = Accounts receivable / Revenue × 365
DIO = Inventory / Cost of goods sold × 365
DPO = Accounts payable / Cost of goods sold × 365
CCC = DSO + DIO − DPO
Operating NWC = Accounts receivable + Inventory − Accounts payable

Cash released = Baseline operating NWC − Target operating NWC
AR release = DSO days reduced / 365 × FY2025 Revenue
Inventory release = DIO days reduced / 365 × FY2025 COGS
AP release = DPO days extended / 365 × FY2025 COGS
```

The target calculator deliberately holds **FY2025 revenue and COGS constant** to isolate the cash effect of changes in the operating cycle.

### Illustrative management scenario (preloaded)

| Metric | FY2025 baseline | Management target |
| --- | ---: | ---: |
| Cash conversion cycle | **116.2 days** | **99.2 days** |
| DSO reduction | — | 5 days |
| DIO reduction | — | 8 days |
| DPO extension | — | 4 days |
| **CCC improvement** | — | **17 days** |

| Source of potential liquidity | Approx. cash release |
| --- | ---: |
| Receivables / collections | **€2.88m** |
| Inventory efficiency | **€3.09m** |
| Payables / supplier terms | **€1.55m** |
| **Total potential cash released** | **€7.51m** |

The model's initial `05_Audit` sheet returns **12 of 12 checks passing**.

## Assumptions & limitations

- This is a **one-time potential balance-sheet liquidity release**, not additional annual revenue or recurring EBITDA.
- DSO / DIO / DPO use **year-end balances as proxies**; actual analysis commonly uses averaged balances and may require separate seasonal diagnostics.
- No ageing schedules, supplier discounts or penalties, implementation costs, taxes, credit-loss changes, operational constraints or full three-statement integration.
- Supplier-payment extension may be commercially infeasible; the model does not verify supplier acceptance.
- The three-day drivers and FY2025 volume base are not forecasts of executable business improvements.
- The audit sheet verifies **internal mechanics**, not data quality or the feasibility of the plan.

## Excel techniques demonstrated

Financial ratio construction · driver-based scenario modelling · dropdown data validation · linked formulas · cash-release bridge · dynamic dashboards · charting · automated reconciliation tests.

---
**Portfolio case study:** entirely fictional inputs for educational demonstration.