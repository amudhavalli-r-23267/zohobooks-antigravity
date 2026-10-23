---
name: books-expenses
description: Record, categorize and analyze Zoho Books expenses, recurring expenses and employees. Use when the user wants to log an expense, attach a receipt, review spending by category or vendor, or set up a repeating expense.
---

## Instructions
1. Resolve expense account (`list_chart_of_accounts`), paid-through account (`list_bank_accounts`), vendor (`list_contacts`) and tax (`list_taxes`). Employees: `list_employees`.
2. `create_expense` with `account_id`, `paid_through_account_id`, `date`, `amount`, optional `vendor_id`, `tax_id`, `reference_number`, `description`, billable flag. Confirm the summary first. Attach files with `add_expense_attachment` or `create_expense_receipt`.
3. Recurring: `create_recurring_expense`; `stop_recurring_expense` / `resume_recurring_expense`; children via `list_child_expenses_of_recurring_expense`.
4. Bank feed: `categorize_bank_transaction_as_expense` when matching an uncategorized bank line.
5. Analysis: `list_expenses` for the period (page through), group by account or vendor, report totals with currency plus top items and outliers.
6. Employees: `create_employee` when logging expenses for staff; `delete_employee` only with explicit confirmation.
7. `update_expense` / `update_recurring_expense` to recategorize or correct. After any write, report the expense id or number, amount, account and currency. `delete_expense` / `delete_recurring_expense` / `delete_expense_receipt` only with explicit confirmation of the specific record.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
