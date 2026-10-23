---
name: books-projects
description: Manage Zoho Books projects, tasks and time entries, including timers and project users. Use when the user wants to create a project, log time, start or stop a timer, or bill project work.
---

## Instructions
1. Resolve customer (`list_contacts`) when the project is client-billed. Users: `list_users`.
2. Project: `create_project` with name, customer (if billable), billing type and users. Confirm first. `clone_project` to copy an existing one. `mark_project_active` / `mark_project_inactive`.
3. Users: `add_project_user` / `invite_project_user` / `update_project_user` / `delete_project_user`.
4. Tasks: `add_project_task` or `add_task`. Status: `mark_task_as_open` / `mark_task_as_ongoing` / `mark_task_as_completed`; `update_percentage_task`. Comments/attachments as needed.
5. Time: `create_time_entries` with project, task, user, date and hours (or start/end). Live timer: `get_running_timer`, `start_entry_timer`, `stop_entry_timer`.
6. Invoices for a project: `list_project_invoices`; create with books-invoicing using project/time line items.
7. Review: `list_projects` / `get_project`; `list_time_entries` / `get_time_entry`. After any write, report the project or time-entry id and hours. Deletes (`delete_project`, `delete_task`, `delete_time_entry`) only on explicit confirmation.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
