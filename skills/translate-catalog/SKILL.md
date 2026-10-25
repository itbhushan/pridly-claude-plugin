---
name: translate-catalog
description: "Find and fill in missing translations of product names, descriptions and SEO text in a multilingual PrestaShop shop. Use when the owner asks which products have no text in a language, or to translate or write product text in French, Spanish, English or any language the shop has."
---

PrestaShop stores product text once per language. Pridly reads and writes each language separately and never overwrites the others.

1. Call `translation_gaps` with the language code (for example `es`). Add `fields` if the owner wants names or SEO texts checked too. It returns the products with the missing text and the existing text in the shop's other languages as the source.
2. If the owner has a saved style, call `get_brand_voice` first and follow it.
3. Write the missing text from the source. Keep the same meaning, facts, numbers and HTML structure (for example `<p>` paragraphs). Do not invent facts, prices, awards or vintages that are not in the source. SEO title: about 60 characters. SEO description: about 150 characters.
4. Call `apply_product_content` with `items`, each `{ id, translations: { es: { description, short_description, ... } } }`, at most 20 products at a time. Only list the languages you are filling in.
5. Show the preview (it is language by language), ask for a clear yes, then confirm. Give the change number and mention that "undo change N" reverses it.
6. At the end say how many products still have gaps and offer the next batch.

Never write a language the shop does not have (the tool lists the shop's languages if you try). Never apply without the owner's yes.
