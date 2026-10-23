---
name: books-fixed-assets
description: Track Zoho Books fixed assets — acquire, activate for depreciation, forecast, sell or write off. Use when the user wants to add an asset, start depreciation, sell an asset, or review asset history.
---

## Instructions
1. Types: `get_fixed_asset_type` / `create_fixed_asset_type` before adding assets of a new class.
2. `create_fixed_asset` with type, name, acquisition date and value, depreciation method/rate as the user specifies. Confirm the summary first. Do not invent depreciation rates.
3. Lifecycle: `mark_fixed_asset_draft` / `mark_fixed_asset_active` (starts depreciation) / `mark_fixed_asset_cancel`. Dispose: `sell_fixed_asset` or `write_off_fixed_asset` — confirm proceeds and date.
4. Review: `list_fixed_assets` / `get_fixed_asset`; `get_fixed_asset_history`; `get_fixed_asset_forecast` for future depreciation.
5. `update_fixed_asset` / `update_fixed_asset_type` after get. After any write, report the asset name, status and value with currency. `delete_fixed_asset` / `delete_fixed_asset_type` only on explicit confirmation naming the asset.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
