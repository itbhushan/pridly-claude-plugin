---
name: safe-bulk-edit
description: "Make changes to many products, prices, stock levels, discounts or discount codes in a PrestaShop shop safely, with a preview first. Use whenever the owner asks to raise or lower prices, change stock or status, run a limited-time sale, create a discount code, or undo or schedule such a change."
---

Every Pridly change tool works in two steps. Follow them exactly.

1. **Preview.** Call the tool WITHOUT `confirm`. It changes nothing and returns a preview and a `preview_id`.
2. **Show and ask.** Show the owner the preview in a short table (product, now, new). Say that nothing has changed yet. Ask a plain yes/no question such as "Apply these changes?".
3. **Apply only after a clear yes.** Then call the same tool with `confirm: true` and the `preview_id`. Never apply on your own, and never reuse an old preview.
4. **Report.** Say what was done and give the change number: "Done. This is change #12. Say 'undo change 12' to put it back."
5. **Undo.** `undo_change` also previews first. Show what will be restored and wait for a yes.

Choosing the right tool:
- Prices, stock, status or categories → `update_products` (prices are excluding tax; product variants move together; stock on products with variants is changed in the PrestaShop back office).
- A sale for a limited time (for example "20% off these products until Sunday 23:59") → `set_product_discount` with `until`. Use `top_products` (order "bottom") first to find slow sellers and pass their ids.
- A discount code → `create_coupon` (percent or fixed amount off the cart; no category restriction).
- Order status or a private note → `update_order`. Changing status can make PrestaShop e-mail the customer: say so in your question. Notes to customers are not possible.
- Later instead of now → confirm with `apply_at` (shop local time, YYYY-MM-DDTHH:MM).

Rules: never change "everything" without a filter; never offer refunds or payments (the owner uses PrestaShop's own tools); never ask for or show Webservice keys; if the preview shows 0 changes or skipped items, say why. If a tool says the key is view-only, explain how to enable editing (Advanced Parameters → Webservice → tick Modify, Add and Delete).
