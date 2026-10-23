---
name: books-credit-notes
description: Issue, apply, refund and review Zoho Books credit notes. Use when the user wants to credit a customer, apply a credit to invoices, refund a credit, or void a credit note.
---

## Instructions
1. Resolve the customer (`list_contacts`), items (`list_items`), taxes (`list_taxes`) and the original invoice (`list_invoices` / `get_invoice`) when the credit relates to one.
2. `create_credit_note` with customer, date, line items (returned items, overpayment or adjustment). Confirm totals and currency first.
3. Lifecycle: `submit_credit_note` / `approve_credit_note`; `mark_credit_note_open` / `mark_credit_note_draft` / `mark_credit_note_void`. Email: `email_credit_note`.
4. Apply to invoices: `apply_credit_note_to_invoice` or `apply_credits_to_invoice`. Review applications with `list_invoices_of_credit_note` / `list_invoice_credits_applied`. Remove with `delete_invoice_applied_credit`.
5. Refund: `create_credit_note_refund`; bank feed: `categorize_as_credit_note_refunds`.
6. `update_credit_note` after `get_credit_note`. After any write, report the credit note number, total, status and currency. `delete_credit_note` / `delete_credit_note_refund` only on explicit confirmation of the credit note number.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
