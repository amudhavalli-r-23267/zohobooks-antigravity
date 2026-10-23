---
name: books-journals
description: Create and review Zoho Books manual journals and chart-of-accounts entries, including publishing a draft journal. Use when the user wants a journal entry, a new ledger account, or to inspect account activity.
---

## Instructions
1. Resolve accounts with `list_chart_of_accounts` / `get_chart_of_account`. Never guess account IDs.
2. Journal: `create_journal` with date, notes and balanced `line_items` (account_id, debit or credit). Debits must equal credits in the org base currency. Confirm the entry table first.
3. Publish a draft with `mark_journal_published`. Comments/attachments: `add_journal_comment`, `add_journal_attachment`.
4. Chart of accounts: `create_chart_of_account` with account type and name; `mark_chart_of_account_active` / `mark_chart_of_account_inactive`. Review activity with `list_chart_of_account_transactions`.
5. Review: `list_journals` / `get_journal`. `update_journal` / `update_chart_of_account` after get.
6. After any write, report the journal number or account name and currency. `delete_journal` / `delete_chart_of_account` only on explicit confirmation. Accounts used on transactions or items cannot be deleted.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
