---
name: monday-check
description: "Weekly shop check-in for a PrestaShop shop. Use when the owner asks how the shop did, how last week or this month went, whether anything needs attention, or wants a quick status report."
---

Give the owner a calm, short weekly check using the Pridly tools. Do not dump raw data.

1. Call `compare_periods` with `period_a` = `last_week` (it compares with the week before by default). If the owner named another period, use that.
2. Call `top_products` for the same period with `limit` 3.
3. Call `store_health_check` and `low_stock_report`.
4. Reply in this shape, in the language the owner writes in:
   - **One sentence** on how the week went (revenue and orders, with the % change).
   - **Top 3 products**, one line each.
   - **Needs attention:** only items with a count above zero (out of stock, orders stuck unpaid or unshipped, missing translations, missing images). Skip anything fine.
   - **One suggested next step**, phrased as a question the owner can say yes to (for example, "Want me to list the products missing a Spanish description?").
5. Amounts are in the shop's currency and exclude VAT unless a tool says otherwise. Say "excl. VAT" once if it matters.
6. If a tool says the Free plan covers only 30 days, mention it once, in one factual line, and move on.

If the owner has several shops, ask which one, or use `multi_store_report` for a one-table summary.
