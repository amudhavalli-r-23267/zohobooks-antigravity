---
name: books-contacts
description: Find, create and update Zoho Books customers and vendors, including contact persons, addresses, portal access, statements, 1099 tracking and CRM import. Use when the user asks to look up a contact, add a customer or vendor, email a statement, or sync from CRM.
---

## Instructions
1. Search with `list_contacts` (name, email, company, status). Use `get_contact` for balances, addresses and terms. `list_contact_persons` / `get_contact_person` for people on the contact.
2. Before creating, search for a match; if found, show it and ask whether to reuse it.
3. `create_contact` needs `contact_name` and `contact_type` (`customer` or `vendor`). Include company, email, phone, currency, payment terms, tax and billing/shipping address when given. Add people with `create_contact_person`; extra addresses with `add_contact_address`.
4. Updates: `update_contact` / `update_contact_person` / `update_contact_address` with only changed fields after confirming. `mark_contact_active` / `mark_contact_inactive`. `mark_contact_person_primary` when asked.
5. Statements and mail: `email_contact_statement` (preview with `get_contact_statement_mail`); `email_contact` for a one-off message. Portal: `enable_contact_portal`. Reminders: `enable_contact_payment_reminder` / `disable_contact_payment_reminder`.
6. US 1099: `track_contact_1099` / `untrack_contact_1099` only when the org country is USA and the user asks.
7. CRM import (requires Books–CRM sync): `import_customer_using_crm_contact_id`, `import_customer_using_crm_account_id`, `import_vendor_using_crm_vendor_id`.
8. After any write, report the contact name, type and id. `delete_contact` / `delete_contact_person` / `delete_contact_address` only on explicit confirmation naming the record. Contacts with transactions may be refused.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
