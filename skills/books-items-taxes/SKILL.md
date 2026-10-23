---
name: books-items-taxes
description: Manage Zoho Books items, pricebooks, taxes, tax groups, authorities and exemptions. Use when the user wants to add or change a product or service, set a price list, or record a tax the user specifies.
---

## Instructions
1. Items: `list_items` / `get_item` / `list_item_details`. Before creating, search for an existing match. `create_item` with `name`, `rate`, `product_type` (`goods` or `service`), optional `sku`, `description`, `unit`, `tax_id`. `mark_item_active` / `mark_item_inactive`. CRM: `import_item_using_crm_product_id` when Books–CRM product sync is on.
2. Pricebooks: `list_pricebooks`; `create_pricebook` / `update_pricebook`; `mark_pricebook_active` / `mark_pricebook_inactive`. Confirm before creating a price list.
3. Taxes: `list_taxes` / `get_tax`; `create_tax` with `tax_name` and `tax_percentage`. Groups: `create_tax_group`. Authorities/exemptions: `create_tax_authority` / `create_tax_exemption` (sales tax must be enabled). Do not advise on tax rates — only record what the user specifies. Taxes in use often cannot be edited or deleted.
4. After any write, report the item or tax name and status.
5. `delete_item` / `delete_pricebook` / `delete_tax` (and tax group/authority/exemption) only on explicit confirmation of the specific record. Items on transactions cannot be deleted.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
