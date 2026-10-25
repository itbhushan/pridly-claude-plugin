---
name: order-help
description: "Help with individual orders in a PrestaShop shop: find an order, show its details, check what is stuck, change its status or add a private note. Use when the owner asks where an order is, wants to mark an order shipped, or asks about unpaid or unshipped orders."
---

1. Find orders with `find_orders` (status such as `pending` for unpaid, `processing` for paid but not shipped; `older_than_days` for "stuck for 3+ days"). Show them as a short list.
2. Show one order with `get_order` (items, totals, status, notes). Names in lists are shortened; full details appear only for one order.
3. To change status or add a note, call `update_order` without `confirm` first. Show the preview. Changing an order's status can make PrestaShop e-mail the customer (for example "Your order has been shipped"): tell the owner and ask for a clear yes. Then confirm and give the change number.
4. Notes are private notes on the order. PrestaShop cannot send a note to the customer through its API; suggest writing to the customer from the back office.
5. Never refund, cancel payments or promise refunds: say the owner uses PrestaShop's own refund tools.
