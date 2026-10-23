---
name: books-invoicing
description: Create, update, send and review Zoho Books invoices, estimates, recurring invoices, retainer invoices, sales receipts, customer debit notes and customer payments. Use when the user wants to bill a customer, send a quote, collect payment, write off a balance, or set up a recurring invoice.
---

## Instructions
1. Resolve the customer with `list_contacts` (type customer), items with `list_items`, and taxes with `list_taxes`. Ask if ambiguous. Review existing docs with `list_invoices` / `get_invoice`.
2. **Invoice:** `create_invoice` with `customer_id`, `date`, `due_date`, `line_items` (item_id or name, quantity, rate, tax_id). From an SO: `create_invoice_from_salesorder`. Confirm the summary (customer, lines, tax, total, currency) first.
3. Lifecycle: `submit_invoice` / `approve_invoice`; `mark_invoice_sent` / `mark_invoice_draft` / `mark_invoice_void`. Email: `email_invoice` or `email_invoices` (max 10). Reminders: `remind_customer_for_invoice_payment`, `bulk_invoice_reminder` (max 10, open/overdue only). Link: `generate_invoice_payment_link`. Write-off: `write_off_invoice` / `cancel_write_off_invoice`.
4. **Estimate:** `create_estimate`; `mark_estimate_sent` / `mark_estimate_accepted` / `mark_estimate_declined`; `email_estimate`.
5. **Recurring invoice:** `create_recurring_invoice`; `stop_recurring_invoice` / `resume_recurring_invoice`; review with `list_recurring_invoices` / `get_recurring_invoice`.
6. **Retainer:** `create_retainer_invoice`; unused credits via `get_unused_retainer_payments`. **Sales receipt:** `create_sales_receipt` for immediate payment. **Debit note:** `create_customer_debit_note` for extra charges on an invoice.
7. **Payment:** `create_customer_payment` with `customer_id`, `amount`, `date`, `payment_mode`, and `invoices` (`invoice_id`, `amount_applied`). Apply existing credits with `apply_credits_to_invoice`. Refund excess with `create_customer_payment_refund`.
8. Changes: `get_*` first, then `update_*` with only changed fields. Paid/sent documents may be restricted.
9. After any write, report the document number, total, status and currency.
10. Deletes (`delete_invoice`, `delete_estimate`, `delete_recurring_invoice`, `delete_retainer_invoice`, `delete_sales_receipt`, `delete_customer_debit_note`, `delete_customer_payment`) require the user to confirm the specific record number.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
