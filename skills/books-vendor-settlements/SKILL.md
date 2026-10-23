---
name: books-vendor-settlements
description: Record vendor payments and vendor credits in Zoho Books — pay bills, apply credits, refund excess, or issue a vendor credit. Use when the user wants to pay a vendor, apply a vendor credit, or refund a vendor overpayment.
---

## Instructions
1. Resolve vendor (`list_contacts`) and open bills (`list_bills`). For credits, resolve items/accounts as needed.
2. **Vendor payment:** `create_vendor_payment` with `vendor_id`, `amount`, `date`, `payment_mode`, and bills to apply (`bill_id`, `amount_applied`). Confirm the allocation first. Email receipt: `email_vendor_payment` (preview `get_vendor_payment_email_content`).
3. **Vendor credit:** `create_vendor_credit` for returns, overpayments or adjustments. Lifecycle: `submit_vendor_credit` / `approve_vendor_credit`; `mark_vendor_credit_open` / `mark_vendor_credit_void`. Apply: `apply_credits_to_bill` / `apply_credits_to_a_bill`.
4. Refunds: `refund_excess_vendor_payment` or `refund_vendor_credit`. Bank feed: `categorize_bank_transaction_as_vendor_payment`, `categorize_as_vendor_payment_refund`, `categorize_as_vendor_credit_refunds`.
5. Review: `list_vendor_payments` / `get_vendor_payment`; `list_vendor_credits` / `get_vendor_credit`.
6. `update_vendor_payment` / `update_vendor_credit` after get. After any write, report the payment or credit number, amount, status and currency. `delete_vendor_payment` / `delete_vendor_credit` / `bulk_delete_vendor_payments` only on explicit confirmation of the specific payment or credit numbers.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
