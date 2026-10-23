# Zoho Books MCP tools

Zoho MCP may expose these as `create_invoice` or `create invoice`. Use the name that appears on the connected global Books server. Call the tool that matches the user prompt.

Confirm organization with `list_organizations` before writes. Show a summary and wait for a yes before create/update/delete.

## Invoices, retainers, recurring invoices

`list_invoices` `get_invoice` `create_invoice` `update_invoice` `delete_invoice`
`create_invoice_from_salesorder` `map_invoice_with_salesorder`
`approve_invoice` `submit_invoice` `mark_invoice_sent` `mark_invoice_draft` `mark_invoice_void`
`write_off_invoice` `cancel_write_off_invoice`
`email_invoice` `email_invoices` `remind_customer_for_invoice_payment` `bulk_invoice_reminder`
`enable_invoice_payment_reminder` `disable_invoice_payment_reminder` `generate_invoice_payment_link`
`get_invoice_email` `get_payment_reminder_mail_content_for_invoice`
`add_invoice_comment` `update_invoice_comment` `delete_invoice_comment` `list_invoice_comments`
`add_invoice_attachment` `get_invoice_attachment` `delete_invoice_attachment` `delete_invoice_document` `get_invoice_document_details` `delete_invoice_expense_receipt` `update_invoice_attachment_preference`
`list_invoice_payments` `delete_invoice_payment` `list_invoice_credits_applied` `apply_credits_to_invoice` `apply_credit_note_to_invoice` `delete_invoice_applied_credit` `delete_invoice_of_credit_note` `list_invoices_of_credit_note`
`list_invoice_templates` `update_invoice_template` `update_invoice_shipping_address` `update_invoice_billing_address` `update_custom_fields_in_invoice` `update_invoice_using_custom_field`
`bulk_export_invoices_as_pdf` `bulk_print_invoices` `list_project_invoices`

`list_retainer_invoices` `get_retainer_invoice` `create_retainer_invoice` `update_retainer_invoice` `delete_retainer_invoice`
`approve_retainer_invoice` `submit_retainer_invoice` `mark_retainer_invoice_sent` `mark_retainer_invoice_draft` `mark_retainer_invoice_void`
`email_retainer_invoice` `get_retainer_invoice_email` `get_unused_retainer_payments`
`add_retainer_invoice_comment` `update_retainer_invoice_comment` `delete_retainer_invoice_comment` `list_retainer_invoice`
`add_retainer_invoice_attachment` `get_retainer_invoice_attachment` `delete_retainer_invoice_attachment`
`list_retainer_invoice_templates` `update_retainer_invoice_template` `update_retainer_invoice_billing_address`

`list_recurring_invoices` `get_recurring_invoice` `create_recurring_invoice` `update_recurring_invoice` `delete_recurring_invoice`
`stop_recurring_invoice` `resume_recurring_invoice` `list_recurring_invoice_history`
`update_recurring_invoice_template` `update_recurring_invoice_using_custom_field`

## Estimates

`list_estimates` `get_estimate` `create_estimate` `update_estimate` `delete_estimate`
`approve_estimate` `submit_estimate` `mark_estimate_sent` `mark_estimate_accepted` `mark_estimate_declined`
`email_estimate` `email_multiple_estimates` `get_estimate_email`
`create_estimate_comment` `update_estimate_comment` `delete_estimate_comment` `list_estimate_comments`
`list_estimate_templates` `update_estimate_template` `update_estimate_shipping_address` `update_estimate_billing_address`
`update_custom_fields_in_estimate` `update_estimate_using_custom_field` `bulk_export_estimates_as_pdf` `bulk_print_estimates`

## Sales orders

`list_sales_orders` `get_sales_order` `create_sales_order` `update_sales_order` `delete_sales_order`
`approve_sales_order` `submit_sales_order` `mark_sales_order_as_open` `mark_sales_order_as_void` `update_sales_order_sub_status`
`email_sales_order` `get_sales_order_email`
`add_sales_order_comment` `update_sales_order_comment` `delete_sales_order_comment` `list_sales_order_comments`
`add_sales_order_attachment` `get_sales_order_attachment` `delete_sales_order_attachment` `update_sales_order_attachment_preference`
`list_sales_order_templates` `update_sales_order_template` `update_sales_order_shipping_address` `update_sales_order_billing_address`
`update_salesorder_customfields` `update_sales_order_using_custom_field` `bulk_export_sales_orders_as_pdf` `bulk_print_sales_orders`

## Delivery challans

`list_delivery_challans` `get_delivery_challan` `create_delivery_challan` `update_delivery_challan` `delete_delivery_challan`
`mark_delivery_challan_as_open` `mark_delivery_challan_as_delivered` `mark_delivery_challan_as_undelivered` `mark_delivery_challan_as_returned`
`return_delivery_challans` `undo_return_delivery_challans`
`add_attachment_to_delivery_challan` `get_delivery_challan_attachment` `delete_delivery_challan_attachment`
`list_delivery_challan_templates` `update_delivery_challan_template` `update_delivery_challan_shipping_address`

## Credit notes and customer debit notes

`list_credit_notes` `get_credit_note` `create_credit_note` `update_credit_note` `delete_credit_note`
`approve_credit_note` `submit_credit_note` `mark_credit_note_draft` `mark_credit_note_open` `mark_credit_note_void`
`email_credit_note` `get_credit_note_email` `get_credit_note_email_history`
`add_credit_note_comment` `delete_credit_note_comment` `list_credit_note_comments`
`create_credit_note_refund` `update_credit_note_refund` `delete_credit_note_refund` `get_credit_note_refund`
`list_credit_note_refunds_of_a_credit_note` `list_credit_note_refunds_of_all_credit_notes` `categorize_as_credit_note_refunds`
`list_credit_note_templates` `update_credit_note_template` `update_credit_note_shipping_address` `update_credit_note_billing_address` `update_credit_note_using_custom_field`

`list_customer_debit_notes` `get_customer_debit_note` `create_customer_debit_note` `update_customer_debit_note` `delete_customer_debit_note`

## Customer payments and sales receipts

`list_customer_payments` `get_customer_payment` `create_customer_payment` `update_customer_payment` `delete_customer_payment` `bulk_delete_customer_payments`
`create_customer_payment_refund` `update_customer_payment_refund` `delete_customer_payment_refund` `get_customer_payment_refund` `list_customer_payment_refunds`
`categorize_bank_transaction_as_customer_payment` `update_custom_fields_in_customer_payment` `update_customer_payment_using_custom_field`

`list_sales_receipts` `get_sales_receipt` `create_sales_receipt` `update_sales_receipt` `delete_sales_receipt` `email_sales_receipt`

## Contacts

`list_contacts` `get_contact` `create_contact` `update_contact` `delete_contact` `update_contact_using_custom_field`
`mark_contact_active` `mark_contact_inactive`
`list_contact_persons` `get_contact_person` `create_contact_person` `update_contact_person` `delete_contact_person` `mark_contact_person_primary`
`get_contact_address` `add_contact_address` `update_contact_address` `delete_contact_address`
`email_contact` `email_contact_statement` `get_contact_statement_mail`
`enable_contact_portal` `enable_contact_payment_reminder` `disable_contact_payment_reminder`
`list_contact_comments` `list_contact_refunds` `track_contact_1099` `untrack_contact_1099`
`import_customer_using_crm_contact_id` `import_customer_using_crm_account_id` `import_vendor_using_crm_vendor_id`

## Purchase orders

`list_purchase_orders` `get_purchase_order` `create_purchase_order` `update_purchase_order` `delete_purchase_order`
`approve_purchase_order` `submit_purchase_order` `reject_purchase_orders` `mark_purchase_order_open` `mark_purchase_order_cancelled` `mark_purchase_order_billed`
`email_purchase_order` `get_purchase_order_email`
`add_purchase_order_comment` `update_purchase_order_comment` `delete_purchase_order_comment` `list_purchase_order_comments`
`add_purchase_order_attachment` `get_purchase_order_attachment` `delete_purchase_order_attachment` `update_purchase_order_attachment`
`list_purchase_order_templates` `update_purchase_order_template` `update_purchase_order_billing_address`
`update_custom_fields_in_purchase_order` `update_purchase_order_using_custom_field` `convert_purchase_order_to_bill`

## Bills and recurring bills

`list_bills` `get_bill` `create_bill` `update_bill` `delete_bill`
`approve_bill` `submit_bill` `mark_bill_open` `mark_bill_void`
`add_bill_comment` `delete_bill_comment` `get_bill_comments`
`add_bill_attachment` `get_bill_attachment` `delete_bill_attachment`
`list_bill_payments` `delete_bill_payment` `apply_credits_to_a_bill` `apply_credits_to_bill` `list_bills_credited` `delete_vendor_credit_bill`
`update_bill_billing_address` `update_custom_fields_in_bill` `update_bill_using_custom_field`

`list_recurring_bills` `get_recurring_bill` `create_recurring_bill` `update_recurring_bill` `delete_recurring_bill`
`stop_recurring_bill` `resume_recurring_bill` `list_recurring_bill_history` `update_recurring_bill_using_custom_field`

## Vendor credits and vendor payments

`list_vendor_credits` `get_vendor_credit` `create_vendor_credit` `update_vendor_credit` `delete_vendor_credit`
`approve_vendor_credit` `submit_vendor_credit` `mark_vendor_credit_open` `mark_vendor_credit_void`
`add_vendor_credit_comment` `delete_vendor_credit_comment` `list_vendor_credit_comments`
`refund_vendor_credit` `update_vendor_credit_refund` `delete_vendor_credit_refund` `get_vendor_credit_refund`
`list_vendor_credit_refunds_of_a_vendor_credit` `list_vendor_credit_refunds_of_all_vendor_credits` `categorize_as_vendor_credit_refunds`

`list_vendor_payments` `get_vendor_payment` `create_vendor_payment` `update_vendor_payment` `delete_vendor_payment` `bulk_delete_vendor_payments`
`email_vendor_payment` `get_vendor_payment_email_content`
`refund_excess_vendor_payment` `update_vendor_payment_refund` `delete_vendor_payment_refund` `get_vendor_payment_refund` `list_vendor_payment_refunds`
`categorize_bank_transaction_as_vendor_payment` `categorize_as_vendor_payment_refund` `update_vendor_payment_using_custom_field`

## Expenses

`list_expenses` `get_expense` `create_expense` `update_expense` `delete_expense` `update_expense_using_custom_field`
`add_expense_attachment` `create_expense_receipt` `get_expense_receipt` `delete_expense_receipt` `list_expense_comments`
`categorize_bank_transaction_as_expense`

`list_recurring_expenses` `get_recurring_expense` `create_recurring_expense` `update_recurring_expense` `delete_recurring_expense`
`stop_recurring_expense` `resume_recurring_expense` `list_child_expenses_of_recurring_expense` `list_recurring_expense_history` `update_recurring_expense_using_custom_field`

`list_employees` `get_employee` `create_employee` `delete_employee`

## Banking

`list_bank_accounts` `get_bank_account` `create_bank_account` `update_bank_account` `delete_bank_account`
`mark_bank_account_active` `mark_bank_account_inactive`
`list_bank_account_rules` `get_bank_account_rule` `create_bank_account_rule` `update_bank_account_rule` `delete_bank_account_rule`
`list_bank_transactions` `get_bank_transaction` `create_bank_transaction` `update_bank_transaction` `delete_bank_transaction`
`get_matching_bank_transactions` `match_bank_transaction` `unmatch_bank_transaction`
`categorize_bank_transaction` `uncategorize_bank_transaction`
`exclude_bank_transaction` `restore_bank_transaction`
`categorize_bank_transaction_as_payment_refund`
`import_bank_statements` `get_last_imported_bank_statement` `delete_last_imported_bank_statement`
`list_chart_of_account_transactions` `delete_chart_of_account_transaction`

## Journals and chart of accounts

`list_journals` `get_journal` `create_journal` `update_journal` `delete_journal` `mark_journal_published`
`add_journal_comment` `delete_journal_comment` `add_journal_attachment`

`list_chart_of_accounts` `get_chart_of_account` `create_chart_of_account` `update_chart_of_account` `delete_chart_of_account`
`mark_chart_of_account_active` `mark_chart_of_account_inactive`

## Fixed assets

`list_fixed_assets` `get_fixed_asset` `create_fixed_asset` `update_fixed_asset` `delete_fixed_asset`
`create_fixed_asset_type` `get_fixed_asset_type` `update_fixed_asset_type` `delete_fixed_asset_type`
`mark_fixed_asset_active` `mark_fixed_asset_draft` `mark_fixed_asset_cancel` `sell_fixed_asset` `write_off_fixed_asset`
`get_fixed_asset_forecast` `get_fixed_asset_history` `create_fixed_asset_comment` `delete_fixed_asset_comment`

## Projects, tasks, time

`list_projects` `get_project` `create_project` `update_project` `delete_project` `clone_project`
`mark_project_active` `mark_project_inactive` `update_projects_using_custom_field`
`add_project_comment` `delete_project_comment` `list_project_comments`
`list_project_users` `get_project_user` `add_project_user` `update_project_user` `delete_project_user` `invite_project_user`
`list_project_tasks` `get_project_task` `add_project_task` `update_project_task` `delete_project_task`

`list_tasks` `get_task` `add_task` `update_a_task` `update_tasks` `delete_task` `delete_tasks`
`mark_task_as_open` `mark_task_as_ongoing` `mark_task_as_completed` `update_percentage_task`
`add_task_comment` `delete_task_comment` `list_task_comments` `add_task_attachment` `get_task_document` `delete_task_document`

`list_time_entries` `get_time_entry` `create_time_entries` `update_time_entry` `delete_time_entry` `delete_time_entries`
`get_running_timer` `start_entry_timer` `stop_entry_timer`

## Items, pricebooks, taxes

`list_items` `list_item_details` `get_item` `create_item` `update_item` `delete_item`
`mark_item_active` `mark_item_inactive` `update_custom_fields_in_item` `update_item_using_custom_field` `import_item_using_crm_product_id`

`list_pricebooks` `create_pricebook` `update_pricebook` `delete_pricebook` `mark_pricebook_active` `mark_pricebook_inactive`

`list_taxes` `get_tax` `create_tax` `update_tax` `delete_tax`
`list_tax_authorities` `get_tax_authority` `create_tax_authority` `update_tax_authority` `delete_tax_authority`
`list_tax_exemptions` `get_tax_exemption` `create_tax_exemption` `update_tax_exemption` `delete_tax_exemption`
`get_tax_group` `create_tax_group` `update_tax_group` `delete_tax_group`
`check_formula_syntax`

## Currencies

`list_currencies` `get_currency` `create_currency` `update_currency` `delete_currency`
`list_exchange_rates` `get_exchange_rate` `create_exchange_rate` `update_exchange_rate` `delete_exchange_rate`
`list_base_currency_adjustments` `get_base_currency_adjustment` `create_base_currency_adjustment` `delete_base_currency_adjustment` `list_base_currency_adjustment_accounts`

## Organization, users, opening balance, locations

`list_organizations` `get_organization` `create_organization` `update_organization`
`list_users` `get_user` `get_current_user` `create_user` `update_user` `delete_user` `invite_user` `mark_user_active` `mark_user_inactive`
`get_opening_balance` `create_opening_balance` `update_opening_balance` `delete_opening_balance`
`list_locations` `create_location` `update_location` `delete_location` `enable_locations` `mark_location_active` `mark_location_inactive` `mark_location_primary`

## Reporting tags

`get_tags` `create_tag` `update_tag` `delete_tag` `reorder_tags` `active_tag` `inactive_tag`
`all_tag_options` `get_all_tag_options` `update_tag_options` `update_tag_criteria` `active_tag_option` `inactive_tag_option` `mark_default_option`

## Customization

`list_custom_fields` `list_custom_fields_simple` `create_custom_field` `update_custom_field` `delete_custom_field`
`reorder_custom_fields` `update_field_status` `update_field_dropdown_options` `get_field_usage` `get_fields_meta` `get_entity_fields_meta` `list_lookup_fields` `get_advance_search_fields` `bulk_fetch_fields`

`list_custom_views` `list_created_views` `get_custom_view` `create_custom_view` `update_custom_view` `delete_custom_view` `reorder_custom_views`

`list_custom_modules` `get_custom_module` `create_custom_module` `update_custom_module` `delete_custom_module`
`list_custom_module_records` `get_custom_module_record` `create_custom_module_record` `update_custom_module_record` `bulk_update_custom_module_records` `delete_custom_module_record` `delete_custom_module_records`

`list_related_lists` `get_related_list` `create_related_list` `update_related_list` `delete_related_list` `reorder_related_lists` `update_related_list_status`

`list_web_tabs` `get_web_tab` `create_web_tab` `update_web_tab` `delete_web_tab` `reorder_web_tabs` `update_web_tab_status`

## Automation

`list_workflows` `get_workflow` `create_workflow` `update_workflow` `delete_workflow`
`activate_workflow` `deactivate_workflow` `reorder_workflows` `trigger_workflow` `trigger_workflow_action`
`get_workflow_editpage` `get_workflow_log_details` `list_workflow_logs` `list_failed_workflows` `list_failed_workflow_actions` `list_upcoming_workflows` `list_upcoming_actions` `get_module_filters`

`list_webhooks` `get_webhook` `create_webhook` `update_webhook` `delete_webhook` `resend_webhook` `bulk_resend_webhooks`
`get_webhook_editpage` `get_webhook_history` `list_webhook_histories`

`list_alerts` `get_alert` `create_alert` `update_alert` `delete_alert` `get_alert_editpage` `get_alert_history` `list_alert_histories`

`list_push_notifications` `get_push_notification` `create_push_notification` `update_push_notification` `delete_push_notification` `get_push_notification_editpage`

`list_custom_triggers` `create_custom_trigger` `update_custom_trigger` `delete_custom_trigger` `execute_custom_trigger` `get_custom_trigger_editpage` `get_custom_trigger_url` `regenerate_custom_trigger_apikey`

`list_retry_policies` `get_retry_policy` `create_retry_policy` `update_retry_policy` `delete_retry_policy`

`list_field_updates` `get_field_update` `create_field_update` `update_field_update` `delete_field_update` `get_field_update_editpage`

`list_custom_functions` `get_custom_function` `create_custom_function` `update_custom_function` `delete_custom_function`
`deploy_custom_function` `download_custom_function` `execute_custom_function` `execute_custom_function_manually` `bulk_execute_custom_functions`
`enable_custom_function_integration` `poll_custom_function_status` `get_custom_function_editpage` `get_custom_function_history` `list_custom_function_histories`

`list_custom_schedulers` `get_custom_scheduler` `create_custom_scheduler` `update_custom_scheduler` `delete_custom_scheduler`

`list_custom_buttons` `get_custom_button` `create_custom_button` `update_custom_button` `delete_custom_button` `list_custom_buttons_meta` `get_custom_button_history`

`list_custom_actions` `get_custom_action` `create_custom_action` `update_custom_action` `delete_custom_action`

`list_blueprints` `get_blueprint` `create_blueprint` `update_blueprint` `delete_blueprint`
