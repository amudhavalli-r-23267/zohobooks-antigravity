---
name: books-banking
description: Manage Zoho Books bank and credit-card accounts, feeds, rules and reconciliation — match, categorize, exclude or restore transactions. Use when the user wants to reconcile a bank line, import a statement, or set up a bank rule.
---

## Instructions
1. Accounts: `list_bank_accounts` / `get_bank_account`. Create with `create_bank_account` (bank or credit card) after confirming name, type and currency. `mark_bank_account_active` / `mark_bank_account_inactive`.
2. Transactions: `list_bank_transactions` / `get_bank_transaction`. Uncategorized first when reconciling.
3. Match existing Books activity: `get_matching_bank_transactions`, then `match_bank_transaction`. Undo with `unmatch_bank_transaction`.
4. Categorize a new line: `categorize_bank_transaction`, or the typed helpers — `categorize_bank_transaction_as_customer_payment`, `categorize_bank_transaction_as_vendor_payment`, `categorize_bank_transaction_as_expense`, `categorize_bank_transaction_as_payment_refund`, `categorize_as_credit_note_refunds`, `categorize_as_vendor_credit_refunds`. Revert with `uncategorize_bank_transaction`.
5. Exclude noise with `exclude_bank_transaction`; bring back with `restore_bank_transaction`.
6. Rules: `list_bank_account_rules`; `create_bank_account_rule` for repeating deposit/withdrawal or refund/charge patterns. Confirm the rule criteria first.
7. Statements: `import_bank_statements`; inspect `get_last_imported_bank_statement`; undo import with `delete_last_imported_bank_statement` only after explicit confirmation.
8. After a match or categorize, report the bank line, action and matched Books record. `delete_bank_account` / `delete_bank_transaction` / `delete_bank_account_rule` only on explicit confirmation naming the account or transaction.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
