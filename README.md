# Alma & Primo Tutorial Index

Step-by-step configuration tutorials for ExLibris Alma and Primo, covering administration, analytics, and discovery setup for library system administrators.

---

## Alma Administration

### General

| Lesson | Synopsis |
|--------|----------|
| [Introduction to Alma Administration](alma-admin/general/final_md/alma_administration_intro_tutorial.md) | Covers administrator roles, the configuration interface, and key online resources for Alma admins. |
| [Integration Profiles](alma-admin/general/final_md/alma_integration_profiles_tutorial.md) | Configure connections to external systems — SIS, ERP, and vendors — using Integration Profiles. |
| [Job Scheduling and Monitoring](alma-admin/general/final_md/alma_job_scheduling_monitoring_tutorial.md) | Schedule and monitor automated Alma jobs for fulfillment, acquisitions, and other processes. |
| [Letters Configuration](alma-admin/general/final_md/alma_letters_configuration_tutorial.md) | Enable, disable, and customize patron and staff letter templates using XSL and label editing. |

---

### Acquisitions

| Lesson | Synopsis |
|--------|----------|
| [Acquisition Methods](alma-admin/acquisitions/final_md/alma_acquisition_methods_tutorial.md) | Configure which acquisition methods (Purchase, Gift, Exchange, etc.) appear on PO Lines and set the default. |
| [Fiscal Period Rollover](alma-admin/acquisitions/final_md/alma_fiscal_period_rollover_tutorial.md) | Run the three sequential rollover jobs to carry ledgers, PO Lines, and resource sharing into a new fiscal period. |
| [License Terms](alma-admin/acquisitions/final_md/alma_license_terms_tutorial.md) | Control which license term sections and individual terms appear on the License Terms tab, including patron-visible terms. |
| [Purchasing and Invoice Rules](alma-admin/acquisitions/final_md/alma_purchasing_invoice_rules_tutorial.md) | Automate the Review and Approval steps of purchasing and invoicing workflows using configurable rules. |
| [Reporting Codes](alma-admin/acquisitions/final_md/alma_reporting_codes_tutorial.md) | Configure five custom PO Line attributes for Analytics reporting and apply them to orders and invoice lines. |

---

### Fulfillment

| Lesson | Synopsis |
|--------|----------|
| [Calendar Management](alma-admin/fulfillment/final_md/alma_calendar_management_tutorial.md) | Manage institution and library open/closed calendars, add closure exceptions, and correct due dates after changes. |
| [Display Logic Rules](alma-admin/fulfillment/final_md/alma_display_logic_rules_tutorial.md) | Control which patron-facing services (Get It, View It, How to Get) appear in Discovery using conditional rules. |
| [Fines and Fees](alma-admin/fulfillment/final_md/alma_fines_fees_tutorial.md) | Understand where fine and fee parameters live within Terms of Use, policies, and rules, and how to update them. |
| [Fulfillment Configuration Utility](alma-admin/fulfillment/final_md/alma_fulfillment_config_utility_tutorial.md) | Use the Fulfillment Configuration Utility to look up the loan terms, due dates, and fines that apply to any patron/item combination without creating a transaction. |
| [Fulfillment Policies and Terms of Use](alma-admin/fulfillment/final_md/alma_fulfillment_policies_tou_tutorial.md) | Build the layered fulfillment model by configuring individual policies and combining them into Terms of Use. |
| [Locations and Transit Time Rules](alma-admin/fulfillment/final_md/alma_locations_transit_times_tutorial.md) | Create and configure physical locations, attach circulation desks, and set transit time rules between libraries. |
| [Overdue and Lost Loan Profiles](alma-admin/fulfillment/final_md/alma_overdue_lost_loan_profiles_tutorial.md) | Set up profiles that send patron notices, apply fines, add blocks, and convert overdue loans to lost at configurable intervals. |
| [Patron and Loan Limits](alma-admin/fulfillment/final_md/alma_patron_loan_limits_tutorial.md) | Define thresholds that block patron accounts and restrict simultaneous checkouts by user group, material type, and location. |
| [User Blocks](alma-admin/fulfillment/final_md/alma_user_blocks_tutorial.md) | Create block descriptions and definitions that restrict patron services when fine, overdue, or account conditions are met. |
| [Work Orders](alma-admin/fulfillment/final_md/alma_work_orders_tutorial.md) | Track items moving through internal processes (preservation, digitization, cataloging) using work order types, statuses, and departments. |

---

### Resources

| Lesson | Synopsis |
|--------|----------|
| [Brief Level Rules](alma-admin/resources/final_md/alma_brief_level_rules_tutorial.md) | Configure rules that assign completeness scores to bibliographic records to protect full records from overlay and enable targeted batch updates. |
| [Call Number Mapping](alma-admin/resources/final_md/alma_call_number_mapping_tutorial.md) | Customize the table that auto-populates call numbers from bibliographic to holdings records, and create holdings templates. |
| [Import Profiles](alma-admin/resources/final_md/alma_import_profiles_tutorial.md) | Set up multi-stage import profiles covering data source, normalization, match/merge, tagging, and inventory creation. |
| [Item Description Templates](alma-admin/resources/final_md/alma_item_description_templates_tutorial.md) | Configure template rules to auto-generate serial item descriptions and sort physical items using sort routines. |
| [Metadata Profiles](alma-admin/resources/final_md/alma_metadata_profiles_tutorial.md) | Edit MARC 21 field/subfield definitions, configure normalization processes, and set up validation rules and exception profiles. |
| [Publishing Profiles](alma-admin/resources/final_md/alma_publishing_profiles_tutorial.md) | Send bibliographic or authority records from Alma to external systems such as OCLC, Primo, and Google Scholar. |
| [Search Index Configuration](alma-admin/resources/final_md/alma_search_indexes_tutorial.md) | Control which search indexes appear in simple and advanced searches, disable unused indexes, and rename local field labels. |

---

### Analytics (Admin)

| Lesson | Synopsis |
|--------|----------|
| [Analytics Introduction — Running and Creating Reports](alma-admin/analytics/final_md/alma_analytics_intro_tutorial.md) | Navigate the Analytics interface, customize existing reports, and build new reports from scratch using Design Analytics. |
| [Analytics Objects](alma-admin/analytics/final_md/alma_analytics_objects_tutorial.md) | Expose Analytics reports to library staff by creating Analytics Objects tied to user roles, dashboards, and scheduled emails. |
| [User Statistics Configuration](alma-admin/analytics/final_md/alma_analytics_user_statistics_tutorial.md) | Configure five custom Statistical Category slots, assign them to user records, and include them in Analytics reports. |

---

## Alma Analytics

| Lesson | Synopsis |
|--------|----------|
| [Running and Creating Reports](alma-analytics/final_md/alma_analytics_running_creating_reports.md) | Use Design Analytics (Oracle Analytics Server) to find overdue items with an existing report and build a new vendor expenditure report. |
| [Analytics Objects](alma-analytics/final_md/alma_analytics_objects.md) | Connect Analytics reports to Alma menus, dashboards, email subscriptions, and homepage widgets via Analytics Objects. |
| [User Statistics](alma-analytics/final_md/alma_analytics_user_statistics.md) | Set up configurable Statistical Category slots, assign values to patrons, and report on custom user data in Analytics. |

---

## Primo VE

| Lesson | Synopsis |
|--------|----------|
| [Views](primo-ve/final_md/alma_primo_views_tutorial.md) | Create and manage Primo VE views that define the patron-facing search interface, results display, and available services. |
| [UI Customization](primo-ve/final_md/alma_primo_ui_customization_tutorial.md) | Brand the Primo VE interface using the Customization Package (CSS/HTML/JS) or Primo Studio visual editor. |
| [Search Configuration](primo-ve/final_md/alma_primo_search_config_tutorial.md) | Configure scopes, search profiles, and slots to control what content is searched and how results are filtered and sorted. |
| [Local Fields and Resource Types](primo-ve/final_md/alma_primo_local_fields_resource_types_tutorial.md) | Map additional bibliographic metadata for search, faceting, and display, and define custom local resource type categories. |
| [Labels and My Library Card](primo-ve/final_md/alma_primo_labels_mylibrarycard_tutorial.md) | Customize patron-facing UI text labels and configure what patrons see on their My Library Card page. |
| [Discovery Import Profiles](primo-ve/final_md/alma_primo_discovery_import_profiles_tutorial.md) | Import external records (XML, Dublin Core, MARC 21) into Primo VE using normalization rules, process tasks, and import profiles. |
| [Delivery Services](primo-ve/final_md/alma_primo_delivery_services_tutorial.md) | Configure Get It request forms, item location display, electronic service links, and How to Get It options for patron access. |

---

## Primo NDE

| Lesson | Synopsis |
|--------|----------|
| [Views (v2)](primo-nde/final_md/alma_primo_views_v2_tutorial.md) | Create and manage Primo VE views in an NDE environment, controlling catalog access and patron-facing configuration. |
| [UI Customization (v2)](primo-nde/final_md/alma_primo_ui_customization_v2_tutorial.md) | Apply institutional branding — logo, favicon, colors, banner, and HTML content — via the Customization Package in an NDE deployment. |
| [Search Configuration (v2)](primo-nde/final_md/alma_primo_search_config_v2_tutorial.md) | Set up scopes, search profiles, slots, resource type filters, and quick filters for patron search in Primo NDE. |
| [Local Fields (v2)](primo-nde/final_md/alma_primo_local_fields_v2_tutorial.md) | Extend search, faceting, and display in Primo NDE by mapping bibliographic metadata to local fields and creating local resource types. |
| [Labels and My Library Activity (v2)](primo-nde/final_md/alma_primo_labels_activity_v2_tutorial.md) | Customize UI label text and configure the patron-facing My Library Activity page in Primo NDE. |
| [Discovery Import Profiles (v2)](primo-nde/final_md/alma_primo_discovery_import_v2_tutorial.md) | Bring external records into Primo NDE discovery using normalization rules, process tasks, and discovery import profile configuration. |
| [Delivery Services (v2)](primo-nde/final_md/alma_primo_delivery_v2_tutorial.md) | Configure request forms, location information display, and electronic service links for patron delivery in Primo NDE. |
