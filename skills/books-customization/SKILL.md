---
name: books-customization
description: Configure Zoho Books custom fields, custom views, custom modules, related lists, reporting tags and web tabs. Use when the user wants a new field, a filtered view, a custom module record, or a reporting tag.
---

## Instructions
1. Inspect first: `list_custom_fields` / `get_entity_fields_meta` / `get_fields_meta` for the entity; `list_custom_modules` / `get_custom_module`; `list_custom_views`; `get_tags`; `list_related_lists`; `list_web_tabs`.
2. **Fields:** `create_custom_field` for a named entity and data type. Dropdown changes: `update_field_dropdown_options`. Activate/deactivate: `update_field_status`. Reorder: `reorder_custom_fields`. Confirm entity, API name and type before creating — schema changes affect every record.
3. **Views:** `create_custom_view` with Zoho filter syntax — dollar-brace placeholders of the form entity.field_name (example: invoice.status; custom fields: invoice.cf_text_field). To match empty/null, use the value PLACEHOLDER.EMPTY. Formula fields: `check_formula_syntax` before saving.
4. **Modules/records:** `create_custom_module` only when the user wants a new module. Records: `list_custom_module_records` / `create_custom_module_record` / `update_custom_module_record` / `bulk_update_custom_module_records`.
5. **Related lists / web tabs:** create/update/reorder/status tools after confirming placement.
6. **Reporting tags:** `create_tag` (starts draft); `active_tag` to use it; `update_tag_options` / `active_tag_option`; `reorder_tags`; `mark_default_option`.
7. After any write, report the entity, name and status. Deletes of fields, modules, views, tags or tabs only on explicit confirmation. Tags/fields in use on transactions often cannot be deleted.

Full tool names: `${PLUGIN_ROOT}/references/mcp-tools.md` (read the matching section only).
