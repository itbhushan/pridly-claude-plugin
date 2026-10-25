# Pridly for PrestaShop

Pridly lets Claude read and manage your PrestaShop shop through the Pridly connector at https://mcp.pridly.gridlypaper.com/mcp. This plugin adds the connector, seven skills that teach Claude your common routines (weekly shop check, safe bulk edits with preview and undo, filling in missing translations, product descriptions in your brand voice, order help, promotion planning, multi-shop reports for agencies) and seven slash commands for the questions owners ask most.

## Use it

1. Connect your shop first, the easy way: install the free Pridly module in your PrestaShop back office (https://pridly.gridlypaper.com/docs/install-module), open its Configure page, click Connect to Pridly and confirm. No keys to copy. Prefer no module? Create a Webservice key (Advanced Parameters → Webservice) and paste it at https://app.pridly.gridlypaper.com/stores.
2. Add this plugin, then connect Pridly from the plugin's Connectors tab and sign in with your email (no password).
3. Type a command, or just ask in your own words, in any language.

## Commands

- `/pridly:weekly-check` the weekly check-in: sales, top products, stock, what to fix.
- `/pridly:low-stock` what is running low, with best sellers first.
- `/pridly:stuck-orders` orders awaiting payment, or paid but not shipped for more than 3 days.
- `/pridly:best-sellers [period]` best and slowest sellers.
- `/pridly:translation-gaps [language]` products with no text in a language, and the missing texts written from your other languages.
- `/pridly:promo-ideas` promotion ideas from your own sales and stock.
- `/pridly:undo [number]` undo a change, with a preview.

Every change shows a preview first and happens only after you say yes. Each change gets a number, and "undo change 12" restores the old values. Other languages are never overwritten. More questions to copy, in English, French and Spanish: https://pridly.gridlypaper.com/prompts

## Data

The plugin contains only instructions and the connector address; it runs no code on your computer. When you use it, your questions' parameters (such as a date range or product ids) go to Pridly, which reads your shop with the key you created and returns the answer. Pridly does not store your orders, products or customers. Privacy policy: https://pridly.gridlypaper.com/privacy

Pridly is an independent product and is not affiliated with or endorsed by PrestaShop. PrestaShop is a trademark of PrestaShop SA.
