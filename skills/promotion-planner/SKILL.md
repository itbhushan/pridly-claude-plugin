---
name: promotion-planner
description: "Plan promotions for a PrestaShop shop from the owner's own numbers: what to put on sale, which discount code to create, which customers went quiet. Use when the owner asks for promotion ideas, a sale, a campaign, or how to sell slow stock."
---

1. Call `suggest_campaigns`. It proposes ideas from recent sales and stock, each with ready-to-use settings. Add `top_products` with order `bottom` for the slowest sellers, and `customer_segments` for customers who went quiet (names are shortened; nothing is sent to anyone).
2. Present 2–3 ideas, each in one or two lines with the reason from the numbers. Ask which one the owner wants.
3. To run a sale use `set_product_discount` (needs an end date); for a code use `create_coupon`. Both preview first: show the preview, ask for a clear yes, then confirm. Give the change number.
4. Pridly does not send e-mails or messages to customers; if the owner wants a mailing, say they send it from their own tool and offer to draft the text.
