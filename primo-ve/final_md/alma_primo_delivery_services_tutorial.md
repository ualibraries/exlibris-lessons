# Primo VE Delivery Services: A Configuration Tutorial

## Overview

Delivery services are how patrons access the items they need in Primo VE — whether physical or electronic. Primo VE provides several delivery service types based on your ALMA inventory, and administrators can configure request forms, item display information, and additional patron-facing services.

---

## The Four Delivery Service Types

Primo VE displays availability information in both brief and full record views. The four delivery types are:

| Service | Description |
|---------|-------------|
| **Get It** | Allows patrons to place requests on physical items. May also include digitization and booking services. |
| **View It** | Displays electronic and digital resources subscribed to or owned by your institution *(out-of-the-box label: View Online)* |
| **How to Get It** | Shown when a record has no inventory; offers options such as purchase requests or resource sharing |
| **Links** | Displays additional links for the resource |

> **Note:** If a record has both print and electronic inventory, both **Get It** and **View It** will appear on the full record display.

---

## Configuring Request Forms

When a patron uses a delivery service (such as Get It or How to Get It), they are prompted to complete a request form. You can customize these forms in ALMA.

Navigate to:

**ALMA Configuration → Discovery → [Get It Configuration section]**

Each form type has its own configuration page. Options vary by form.

### Example: Customizing a Digitization Request Form

1. Open the **Digitization Request** configuration page.
2. For each field, choose whether it is **visible** and/or **mandatory**.
3. To add a custom checkbox field:
   - Locate the **generic checkbox field**
   - Set **Display to Public** to *Yes*
   - Check the box to make it **mandatory** if required
4. Click **Save**.

### Updating the Label for a Custom Field

After adding a custom field, update its display label in Primo VE:

1. Navigate to: **Discovery → Display Configuration → Labels**
2. Find the table for your form's labels (e.g., *Digitization Labels*)
3. Open the Row Action tool → **Customize**
4. Locate the generic field entry
5. Open its Row Action tool → **Customize**
6. Change the **description** to the text you want displayed in Primo VE
7. Click **Customize** to save

---

## Configuring the Get It Item Display

Navigate to:

**ALMA Configuration → Discovery → Get It Configuration → Items Display Configuration**

This page has two sections:

- **Brief Item Display** — the summary shown in the results list
- **Full Item Display** — the detailed view shown on the full record page

For each section:
- Use the **toggle buttons** to activate or deactivate individual lines
- Use the Row Action tool → **Edit** to change the label or field content
  - In the edit pop-up, select **No Label** or **Not Defined** to show no label
  - Click **Add Field** to include additional information, then select from the drop-down
  - Click **Add Field** to confirm, then **Done** when finished

---

## Configuring General Electronic Services (How to Get It Links)

General Electronic Services define additional links shown in the **How to Get It** section (and optionally in **View It** or **Get It**) for resources not owned or subscribed to by your institution.

Navigate to:

**ALMA → Fulfillment → Discovery Interface Display Logic → General Electronic Services**

This page lists all currently configured services. Use toggles to activate/deactivate, or the Row Action tool to **Edit**.

### Creating a New General Electronic Service

Click **Add Service** and fill in:

| Field                       | Description                                                                                  |
| --------------------------- | -------------------------------------------------------------------------------------------- |
| **Service Code and Name**   | Internal identifiers                                                                         |
| **Description**             | Optional internal note                                                                       |
| **Public Name**             | The label displayed to patrons in Primo VE                                                   |
| **Public Note**             | Text displayed beneath the public name                                                       |
| **Document Delivery / ILL** | Select *Yes* to list in How to Get It or Get It; select *No* to list in the Links section    |
| **Display Location**        | If ILL/document delivery, choose where to display (e.g., *Get It and How to Get It*)         |
| **URL Template**            | The URL where patrons will be redirected                                                     |
| **Item Level**              | *Yes* = a link appears next to each matching item; *No* = link appears at the holdings level |

Click **Add and Close** when done.

### Configuring Service Availability Rules

After creating a service, open its Row Action tool → **Edit** to configure **Service Availability Rules** (the conditions under which the service is displayed).

> **Important:** Input parameters are optional, but by default, service availability is always **False** — the service will **never** display in Primo VE unless you configure availability rules.

---

## Ordering Electronic Service Links

To change the display order of electronic service links:

Navigate to:

**ALMA → Fulfillment → Discovery Interface Display Logic → General Electronic Services Order**

- Use the **up and down arrows** to rearrange services in the list
- Click **Add to Top** and use the drop-down to add a new service at the top of the order
- Use the **Services to Be Placed Last** section to anchor specific services at the bottom of the list

---

## Summary

Primo VE delivery service configuration gives you full control over how patrons access resources — from the content of request forms to the links shown when no inventory exists. By configuring request forms, item display layouts, and general electronic services (and their order), you can create a seamless and institution-appropriate resource access experience for your users.
