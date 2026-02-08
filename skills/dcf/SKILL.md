---
name: dcf-valuation
description: Perform discounted cash flow valuation to estimate intrinsic value and implied upside or downside.
---

# DCF Valuation

## Trigger
Use for fair value, intrinsic value, valuation, DCF, price target, overvalued/undervalued prompts.

## Checklist
1. Collect cash flow history (5+ years).
2. Collect latest balance sheet and share count.
3. Collect current price and key metrics.
4. Estimate growth and discount rate assumptions.
5. Project 5-year free cash flow and terminal value.
6. Discount to present value and compute per-share fair value.
7. Run sensitivity table (WACC +/-1%, terminal growth 2.0/2.5/3.0%).
8. Validate reasonableness and present caveats.

## Required Data
1. Free cash flow (or CFO and capex to derive FCF)
2. Total debt and cash
3. Shares outstanding
4. Current market price
5. Sector or risk profile for WACC assumption

## Guardrails
1. Cap long-run growth assumptions to realistic ranges.
2. Show assumptions explicitly.
3. If required data is missing, state fallback method and confidence impact.

## Output
1. Valuation summary: fair value, market price, implied upside/downside.
2. Inputs table: assumptions and sources.
3. Projection table: yearly FCF and present values.
4. Sensitivity matrix.
5. Caveats and confidence statement.
