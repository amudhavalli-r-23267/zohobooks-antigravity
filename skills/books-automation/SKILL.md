---
name: books-automation
description: Configure Zoho Books workflows, webhooks, alerts, custom functions, schedulers, buttons, field updates and blueprints. Use when the user wants to automate a Books action, inspect failed workflows, or manage a webhook.
---

## Instructions
1. Inspect first: `list_workflows`, `list_webhooks`, `list_alerts`, `list_custom_functions`, `list_custom_schedulers`, `list_custom_buttons`, `list_field_updates`, `list_blueprints`, `list_failed_workflows`, `list_upcoming_workflows`.
2. Workflows: `create_workflow` after the user names the module, trigger and actions. Activate/deactivate with `activate_workflow` / `deactivate_workflow`. Manual run: `trigger_workflow`. Reorder: `reorder_workflows`.
3. Webhooks: `create_webhook`; failed deliveries `list_webhook_histories` / `resend_webhook` / `bulk_resend_webhooks`. Confirm the URL and event before creating.
4. Alerts and push: `create_alert` / `create_push_notification`. Field updates: `create_field_update`. Custom triggers: `create_custom_trigger` / `execute_custom_trigger` — regenerating a key (`regenerate_custom_trigger_apikey`) invalidates the old one; confirm first.
5. Functions: `create_custom_function` / `deploy_custom_function` / `execute_custom_function`. Schedulers: `create_custom_scheduler`. Buttons/actions: `create_custom_button` / `create_custom_action`. Blueprints: `create_blueprint`.
6. Treat automation writes as high-impact. Show trigger, module, actions and any URL/code summary and wait for a yes. Prefer updating an existing workflow over creating a duplicate.
7. After any write, report the workflow or action name and status. Deletes of workflows, webhooks, functions, buttons or blueprints only on explicit confirmation naming the record.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
