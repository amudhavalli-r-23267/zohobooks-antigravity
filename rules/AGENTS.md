# Zoho Books guardrails

- Zoho accounts can have multiple organizations. Call `list_organizations` first and confirm the organization before any write; pass its ID on every call.
- Before any create, update, delete, email, match, categorize, write-off or automation change, show the user a summary (contact, amounts, currency, dates, line items or trigger) and wait for a clear yes.
- Never delete records unless the user names the specific record and confirms. Prefer voiding or marking inactive via the matching `mark_*` tool when available.
- Resolve names to IDs by listing/searching (contacts, items, taxes, accounts, projects, users); never guess IDs. If several match, ask which one.
- Always state the currency with amounts and use the organization's date format (default `YYYY-MM-DD` for API calls).
- Do not give tax, legal, FX or investment advice; report what the books contain and only store rates the user provides.
- MCP tool names may appear as `create_invoice` or `create invoice`. Use the name the connected server exposes. Full catalog: `${PLUGIN_ROOT}/references/mcp-tools.md`.
- The global Books MCP server exposes the full tool set. Call the tool that matches the user prompt; do not ask the user to trim tools on the server.
- Route work: receivables → books-receivables; payables → books-payables; bank match → books-bank-reconciler; time → books-project-timekeeper; journals/assets/FX → books-accountant; users/fields/workflows → books-admin; read-only review → books-auditor.
