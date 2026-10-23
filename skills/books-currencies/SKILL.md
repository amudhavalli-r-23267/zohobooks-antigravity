---
name: books-currencies
description: Manage Zoho Books currencies, exchange rates and base-currency adjustments. Use when the user wants to add a currency, set a rate, or post a base-currency adjustment.
---

## Instructions
1. `list_currencies` / `get_currency` to see configured currencies and whether they are live.
2. `create_currency` with code and symbol when the user names a currency that is missing. `update_currency` for format/rate settings.
3. Rates: `list_exchange_rates` / `get_exchange_rate`; `create_exchange_rate` / `update_exchange_rate` for a date-effective rate the user provides. Do not invent FX rates.
4. Period-end: `list_base_currency_adjustment_accounts` for accounts affected by a rate, then `create_base_currency_adjustment`. Confirm accounts, rate and date first.
5. After any write, report the currency code or adjustment id and rate. `delete_currency` / `delete_exchange_rate` / `delete_base_currency_adjustment` only on explicit confirmation. Currencies used on transactions cannot be deleted.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
