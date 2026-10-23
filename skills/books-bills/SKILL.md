---
name: books-bills
description: Record, approve and review Zoho Books vendor bills and recurring bills. Use when the user wants to enter a vendor bill, convert a purchase order to a bill, apply vendor credits, or set up a repeating bill.
---

## Instructions
1. Resolve vendor (`list_contacts`), items (`list_items`), expense/asset accounts (`list_chart_of_accounts`) and taxes (`list_taxes`).
2. `create_bill` with `vendor_id`, `bill_number` or auto-number, `date`, `due_date`, `line_items`. From PO: `convert_purchase_order_to_bill` then `create_bill`. Confirm totals and currency first.
3. Lifecycle: `submit_bill` / `approve_bill`; `mark_bill_open` / `mark_bill_void`. Comments/attachments: `add_bill_comment`, `add_bill_attachment`.
4. Credits: `apply_credits_to_bill` (vendor credits or excess vendor payments). Review `list_bill_payments` / `list_bills_credited`.
5. Recurring: `create_recurring_bill`; `stop_recurring_bill` / `resume_recurring_bill`; `list_recurring_bills` / `get_recurring_bill`.
6. Pay a bill with `create_vendor_payment` (books-vendor-settlements). After any write, report the bill number, total, status and currency.
7. `update_bill` / `update_recurring_bill` after get. Bills with payments cannot be deleted. `delete_bill` / `delete_recurring_bill` only on explicit confirmation of the bill number.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
