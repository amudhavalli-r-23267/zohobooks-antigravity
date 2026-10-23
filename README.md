# Zoho Books for Antigravity

Run Zoho Books from chat: sales and purchases, banking, journals, projects, items, taxes, customization and automation.

## Setup

1. Install the plugin. It connects to the global Books MCP server at <https://books.zohomcp.com/mcp/message>.
2. Authorize the Zoho Books connection when prompted.
3. Skills and agents pick the matching tool from the user prompt. The full Books tool set can stay enabled on that server.

```bash
agy plugin validate .
agy plugin install .
```

## Skills

| Command | What it does |
| --- | --- |
| `/books-account-overview` | Org, users, opening balance, locations, CoA, AR/AP snapshot, P&L-style insights |
| `/books-contacts` | Customers and vendors, persons, portal, statements, 1099, CRM import |
| `/books-invoicing` | Invoices, estimates, recurring and retainer invoices, sales receipts, debit notes, customer payments |
| `/books-sales-orders` | Sales orders and delivery challans |
| `/books-credit-notes` | Credit notes, apply to invoices, refunds |
| `/books-purchases` | Purchase orders and convert PO to bill |
| `/books-bills` | Bills and recurring bills |
| `/books-vendor-settlements` | Vendor payments and vendor credits |
| `/books-expenses` | Expenses, recurring expenses, receipts, employees |
| `/books-banking` | Bank accounts, feeds, rules, match and categorize |
| `/books-journals` | Manual journals and chart of accounts |
| `/books-fixed-assets` | Asset types, depreciation, sell and write-off |
| `/books-projects` | Projects, tasks, time entries and timers |
| `/books-items-taxes` | Items, pricebooks, taxes, groups, authorities, exemptions |
| `/books-currencies` | Currencies, exchange rates, base-currency adjustments |
| `/books-customization` | Custom fields, views, modules, related lists, reporting tags, web tabs |
| `/books-automation` | Workflows, webhooks, alerts, functions, schedulers, buttons, blueprints |

Full MCP tool names by module: [references/mcp-tools.md](references/mcp-tools.md).

## Agents

Delegate these from chat when the work is a focused review or write in one domain.

| Agent | Role |
| --- | --- |
| `books-auditor` | Read-only review: overdue docs, duplicates, uncategorized bank lines |
| `books-receivables` | Collect, remind, apply credits, record customer payments |
| `books-payables` | Enter bills, pay vendors, apply vendor credits |
| `books-bank-reconciler` | Match and categorize bank transactions |
| `books-project-timekeeper` | Projects, tasks, timers, unbilled hours |
| `books-accountant` | Journals, CoA, FX adjustments, fixed assets |
| `books-admin` | Users, locations, custom fields, workflows |

## Safety

Create/update/email/match actions are confirmed with you before they run. Delete actions always require explicit confirmation of the named record.
