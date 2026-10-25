---
description: "Orders that are awaiting payment or paid but not shipped for more than 3 days"
---

Call `find_orders` with `older_than_days` 3 for the statuses that mean "awaiting payment" and for the statuses that mean "paid but not yet shipped" in this shop.

Reply with two short lists, "Waiting for payment" and "Paid but not shipped", each with order number, date, total and how many days old. If both are empty, say the shop is clear. Offer to add a private note to a specific order, but change nothing until I say yes.
