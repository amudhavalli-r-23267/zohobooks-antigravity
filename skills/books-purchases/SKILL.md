---
name: books-purchases
description: Create, approve, email and review Zoho Books purchase orders, including converting a PO to a bill. Use when the user wants to order from a vendor, check open POs, or mark a PO billed.
---

## Instructions
1. Resolve the vendor (`list_contacts`, type vendor), items (`list_items`) and taxes (`list_taxes`). Ask if several match.
2. `create_purchase_order` with `vendor_id`, `date`, `delivery_date`, `line_items`. Confirm totals and currency first.
3. Lifecycle: `submit_purchase_order` / `approve_purchase_order` / `reject_purchase_orders`; `mark_purchase_order_open` / `mark_purchase_order_cancelled` / `mark_purchase_order_billed`. Email: `email_purchase_order`.
4. Convert to bill: `convert_purchase_order_to_bill` (fetch payload from PO ids, then `create_bill`).
5. Review: `list_purchase_orders` / `get_purchase_order`; comments and attachments via `list_purchase_order_comments`, `add_purchase_order_comment`, `add_purchase_order_attachment`.
6. `update_purchase_order` with only changed fields after `get_purchase_order`. After any write, report the PO number, total, status and currency. `delete_purchase_order` only on explicit confirmation of the PO number.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
