---
description: "Weekly check of my shop: sales, top products, stock and what to fix"
---

Give me my weekly shop check using the Pridly tools. Follow the monday-check skill if it is available.

1. Call `compare_periods` for `last_week` against the week before.
2. Call `top_products` for `last_week` with `limit` 3.
3. Call `store_health_check` and `low_stock_report`.
4. Reply in my language with one sentence on how the week went (revenue, orders and the % change), my top 3 products, only the items that need attention, and one suggested next step as a yes/no question. Prices are excluding VAT.
