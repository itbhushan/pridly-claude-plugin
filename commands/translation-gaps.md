---
description: "Products with no text in a language, and the missing texts written from your other languages"
argument-hint: "[language code, for example es or fr]"
---

Use the language "$ARGUMENTS" if I gave one, otherwise ask me which language to check.

1. Call `translation_gaps` for that `language` with `limit` 20.
2. List the products that are missing text, with the existing text in the shop's other languages.
3. Ask whether I want the missing texts written. If I say yes, call `get_brand_voice` first, write them in my saved style, and show the usual preview before saving anything. Other languages of a product must never be overwritten.
