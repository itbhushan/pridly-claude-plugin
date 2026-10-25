---
name: product-descriptions
description: "Write or improve product descriptions in a PrestaShop shop in the owner's brand voice. Use when the owner wants better, longer or more consistent product text, or asks for descriptions for products that have none."
---

1. Call `get_brand_voice` and follow the saved style. If none is saved, ask for the tone in one line, then offer to save it with `save_brand_voice`.
2. Find the products: `find_products` with `max_description_words` (for example 30) or `missing: ["description"]`; the owner can also name products.
3. Write the new text in the shop's main language (and other languages only if asked): short description 1–2 sentences, description 2–4 short paragraphs in `<p>` tags. Use only facts that are in the shop data or that the owner gave. Do not invent awards, ingredients or years.
4. Save with `apply_product_content`: `items: [{ id, translations: { <lang>: { name?, short_description, description, meta_title?, meta_description? } } }]`, at most 20 at a time.
5. It shows a before/after preview. Show a few examples, ask for a clear yes, then confirm. Give the change number; "undo change N" restores the old text.

Other languages stay untouched. If other languages are missing, offer the `translate-catalog` routine next.
