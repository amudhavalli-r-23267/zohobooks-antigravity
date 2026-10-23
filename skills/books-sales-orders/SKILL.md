---
name: books-sales-orders
description: Create, approve, fulfill and review Zoho Books sales orders and delivery challans. Use when the user wants to confirm a customer order, ship goods, mark a challan delivered or returned, or convert an order toward an invoice.
---

## Instructions
1. Resolve the customer (`list_contacts`, type customer), items (`list_items`) and taxes (`list_taxes`). Ask if several match.
2. **Sales order:** `create_sales_order` with `customer_id`, `date`, `shipment_date`, `line_items`. Confirm totals and currency first.
3. Lifecycle: `submit_sales_order` / `approve_sales_order`; `mark_sales_order_as_open` / `mark_sales_order_as_void`; `update_sales_order_sub_status`. Email: `email_sales_order`. Invoice from SO: `create_invoice_from_salesorder` or `map_invoice_with_salesorder`.
4. **Delivery challan:** `create_delivery_challan` (requires customer). Status: `mark_delivery_challan_as_open` / `mark_delivery_challan_as_delivered` / `mark_delivery_challan_as_undelivered` / `mark_delivery_challan_as_returned`. Partial returns: `return_delivery_challans` / `undo_return_delivery_challans`.
5. Review: `list_sales_orders` / `get_sales_order`; `list_delivery_challans` / `get_delivery_challan`. Attachments and comments as needed.
6. `update_sales_order` / `update_delivery_challan` after get. After any write, report the document number, total, status and currency. `delete_sales_order` / `delete_delivery_challan` only on explicit confirmation of the document number. Invoiced SOs cannot be deleted.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
