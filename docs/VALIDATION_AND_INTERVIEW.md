# Model checks and interview discussion

## Validation procedure

Open `models/Working_Capital_Release_CCC_Optimizer_Completed.xlsx` in Excel, then:

1. Confirm FY2024 and FY2025 historical figures in `01_Historical` are synthetic inputs.
2. Check **DSO = A/R ÷ revenue × 365**, **DIO = inventory ÷ COGS × 365**, **DPO = A/P ÷ COGS × 365**.
3. Confirm **CCC = DSO + DIO − DPO** in each year.
4. On `04_Dashboard`, select **Management** and confirm CCC falls from **116.2** to **99.2** days.
5. Confirm individual improvements: **DSO −5 days**, **DIO −8 days**, **DPO +4 days**.
6. Verify the potential cash release: **€2.88m** from collections, **€3.09m** from inventory, **€1.55m** from supplier terms; total **€7.51m** (rounding may differ).
7. Inspect `03_Cash_Bridge`; the total release must equal baseline operating NWC minus target NWC.
8. Check `05_Audit` shows **12 of 12 PASS** with initial inputs.
9. Toggle **Conservative** and **Stretch** scenarios. Ensure the dashboard, calculations and audit tests update.
10. Modify one day lever on `02_Targets` and check the related euro release uses FY2025 sales or COGS as appropriate.

## Formula interpretation

| Lever | Change | Source of financing |
| --- | --- | --- |
| DSO decreases | Lower receivables | Collect customer cash sooner |
| DIO decreases | Lower inventory | Hold less capital in stock |
| DPO increases | Higher payables | Pay suppliers later |

The model separates operating-cycle improvement from the scale effects of growing revenue/COGS by holding the FY2025 values fixed in targets.

## What the model does NOT prove

The €7.51m is an **illustrative one-off potential liquidity release**. It is not recurring EBITDA or guaranteed free cash flow. Executing supplier extensions or inventory cuts may affect relationships, service levels, stock-outs, discounts or costs. Historical DSO/DIO/DPO use year-end proxy balances and may be distorted by seasonality.

## Suggested interview questions

- Why does raising DPO release cash but lowering DSO/DIO also release cash?
- Why does working capital release not directly increase EBITDA?
- Why do operating ratios change if you use average rather than year-end balances?
- How would you account for seasonal demand or different trade terms?
- What practical constraints might prevent achieving the Stretch scenario?
