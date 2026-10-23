---
name: books-account-overview
description: Overview of a Zoho Books organization — org details, users, opening balance, locations, chart of accounts, receivables/payables, profit and loss style insights, revenue and top expenses. Use when the user asks how the business is doing, P&L, what is overdue, who has access, or wants org/account lookups.
---

## Instructions
1. Call `list_organizations`; if more than one, ask which to use. Use `get_organization` for base currency and fiscal settings. `get_current_user` for the signed-in user.
2. Receivables: `list_invoices` filtered by status (`overdue`, `unpaid`, `partially_paid`); total per customer and in aggregate. Payables: `list_bills` for unpaid/overdue. State currency and date range.
3. Activity: `list_customer_payments`, `list_vendor_payments`, `list_expenses` for the requested period. Page through (`page`/`per_page`) before totalling.
4. Lookups: `list_bank_accounts`, `list_chart_of_accounts`, `list_users`, `list_locations`, `get_opening_balance`, `get_tags`.
5. Insights (no dedicated report tools): derive period totals from lists — billed (`list_invoices`), collected (`list_customer_payments`), spent (`list_expenses` + `list_bills`), top customers/vendors. Present a concise table.
6. Writes (`update_organization`, `create_user`/`invite_user`/`mark_user_active`/`mark_user_inactive`/`delete_user`, `create_opening_balance`/`update_opening_balance`/`delete_opening_balance`, `create_location`/`enable_locations`/`mark_location_primary`) need an explicit summary and yes. Prefer not creating extra organizations.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
