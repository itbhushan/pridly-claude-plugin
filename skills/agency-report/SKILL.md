---
name: agency-report
description: "One-table report across several PrestaShop shops for agencies and owners with more than one shop. Use when the owner asks for a summary of all their shops, a client report, or month-end numbers per shop."
---

1. Call `multi_store_report` (optionally with a `period`, such as `last_month`). It returns revenue, orders and the top product for every connected shop.
2. Present one table: shop, revenue, orders, top product. Add one sentence on the best and the weakest shop. State the currency of each shop; do not add amounts in different currencies together.
3. If a shop failed to load, say which and why (the tool explains it) and continue with the rest.
4. The multi-shop report needs the Agency plan; if the tool says so, mention it once with the factual line it gives.
