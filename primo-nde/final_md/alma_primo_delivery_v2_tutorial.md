# Primo VE Delivery Services: Request Forms, Location Information, and Links

## Overview

Delivery services in Primo VE are how patrons access the items they want. These services are based on your ALMA inventory. Some availability information is visible in the brief record, but the full record provides the complete picture.

This tutorial covers configuration of the three delivery service sections that appear in the full record:

1. **Request Forms** — forms patrons fill out to place requests
2. **Location Information** — where to find physical items
3. **Electronic Service Links** — additional links such as Google Books, ILL services, and more

---

## Part 1: Configuring Request Forms

When patrons request an item, they complete a request form. Several form types can be customized.

Navigate to:

**ALMA Configuration → Discovery → Get It Configuration**

Available forms include:
- Digitization Request
- Hold and Booking Request
- Purchase Request
- Resource Sharing Request

### Example: Customizing the Digitization Request Form

1. Select **Digitization Request**.
2. For each field, choose whether it is **visible** and/or **mandatory**.
3. To make the **copyright declaration** mandatory, toggle it on.
4. To add a **custom checkbox** field:
   - Locate the **generic checkbox** field
   - Set **Display to Public** to *Yes*
   - Leave mandatory unchecked if it should be optional
5. Click **Save**.

### Adding a Label to the Custom Checkbox

The checkbox appears but displays no text until you add a label.

1. Navigate to: **ALMA Configuration → Discovery → Display Configuration → Labels**
2. Find the label table for your form (e.g., *Digitization Labels*)
3. Open the Row Action menu → **Customize**
4. Find **Alma Digitization, Generic Checkbox**
5. Change the **Description** — this becomes the text displayed next to the checkbox in Primo VE
6. While in the same table, you can also update the **form description** label
7. Click **Save**

The customized form will appear when patrons request a digitization, showing the new description and checkbox alongside the out-of-the-box copyright statement.

---

## Part 2: Configuring Location Information

Location information tells patrons where to find physical items. It appears in two places:

- **Brief Item Display** — visible even when the section is collapsed
- **Full Item Display** — the expanded, detailed view

Navigate to:

**ALMA Configuration → Discovery → Get It Configuration → Items Display Configuration**

### Editing a Row

1. Click the Row Action menu → **Edit**.
2. Options include:
   - Change the **label** displayed (or select *Not Defined* to show no label)
   - Click the **globe icon** to assign different labels for different languages
3. Click **Done**.

### Adding a Field to the Full Item Display

1. Click **Add Field**.
2. Select the desired field from the drop-down.
3. Add a **label** if desired.
4. Click **Done**.

Changes are visible in Primo VE in both the brief results list and the full record view.

---

## Part 3: Configuring Electronic Service Links

General Electronic Services are flexible links added to the full record, such as searching for a book on Google, ordering via Amazon, or accessing ILL through Iliad.

Navigate to:

**ALMA → Fulfillment → Discovery Interface Display Logic → General Electronic Services**

This page lists all configured services. Toggle to activate/deactivate or use the Row Action menu to **Edit**.

### Creating a New Service

Click **Add Service** and fill in:

| Field | Description |
|-------|-------------|
| **Service Code / Name** | Internal identifiers |
| **Description** | Optional internal note |
| **Public Name** | The label displayed to patrons |
| **Public Note** | Text shown beneath the public name |
| **Document Delivery / ILL** | *Yes* = shown in Request or View Online sections; *No* = shown in Links section |
| **Display Location** | If ILL/Doc Delivery, choose where to display (e.g., Request section, View Online section) |
| **URL Template** | The web address patrons are redirected to when clicking the link |

Click **Add and Close**.

### Configuring Service Availability Rules

After creating a service, open its Row Action menu → **Edit** to configure when it displays.

> **Important:** By default, the General Electronic Services rule sets **Display to False**, meaning the service will **not appear** in Primo VE until you configure a display rule.

To add a display rule:
1. Click **Add Rule**.
2. Enter a **name**.
3. Click **Add Parameter** to define an **input condition** (e.g., ISBN field is not empty).
4. Click **Add Parameter** to confirm.
5. For the **Output Parameter**, select **True** — the service will display when the condition is met.

**Example:** A service that displays only when an ISBN is present in the record.

> For more information on managing Display Logic rules, see the Knowledge Center.

### Managing Service Link Order

Navigate to:

**ALMA → Fulfillment → Discovery Interface Display Logic → General Electronic Services Order**

There are also separate configuration pages for ordering:
- Digital viewers
- Online services
- Locations

---

## Summary

Primo VE's delivery configuration gives you precise control over the patron request experience. Customized request forms with descriptive labels and relevant fields, clearly organized location information, and well-configured electronic service links all contribute to a seamless and institution-specific delivery workflow.
