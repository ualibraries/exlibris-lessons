# ALMA Work Orders: A Configuration Tutorial

## Overview

Work orders allow you to track physical items as they move through internal library processes such as preservation, cataloging, or digitization. When an item's barcode is scanned into a work order, ALMA:

- Sends the item to the assigned department
- Updates the item status to *Item Not in Place*
- Still allows patrons to place future requests on the item

Work orders can be tracked alongside patron requests on the **Resource Request Monitoring** page (use the facet for *Request Process Type* to filter by work order type).

### Work Order Components

| Component | Description |
|-----------|-------------|
| **Type** | The category of library process (e.g., Preservation, Digitization, Cataloging) |
| **Status** | Tracks progress within a type (e.g., for Preservation: Gluing, Sewing; for Digitization: Digitizing, Document Delivery) |
| **Department** | The physical location in the library where the work is being performed |

Work orders can be created at the **institution** or **library** level, but can only be **attached to a circulation desk at the library level**.

> **Note:** The out-of-the-box **ACK Work Order** type is tied to Acquisitions functionality. You can manage its statuses and edit it, but you cannot manage departments or delete it.

---

## Step 1: Create a Work Order Type

Navigate to:

**ALMA Configuration → General → Work Orders and Departments → Work Order Types**

This page lists all current work order types.

### Adding a New Type

1. Click **Add Work Order Type**.
2. Enter a **Code**, **Name**, and optional **Description**.
3. Check or uncheck **Recalls Loans** — determines whether this work order type can recall active loans. For a preservation work order, for example, you would typically uncheck this.
4. Click **Add Work Order Type**.

### Managing Existing Types

From the **Row Action** tool, you can:
- **Manage Statuses** — add or edit the statuses within this type
- **Manage Departments** — add or edit the departments associated with this type
- **Edit** — change the name, description, or recall loans setting
- **Remove** — delete the work order type

---

## Step 2: Add Statuses to the Work Order Type

1. From the Row Action tool of your new work order type, select **Manage Statuses**.
2. Click **Add Status**.
3. Enter a **Code** and **Name** (required), and optional description.
4. Click **Add Status**.
5. Repeat for each additional status.

> Statuses are saved automatically as you add them.

6. Click the **back arrow** when finished.

---

## Step 3: Create a Work Order Department

A department represents where the work will be completed. There are two ways to access department creation:

- **Option A:** Go to **General → Work Orders and Departments → Work Order Departments**, then click **Add Department**
- **Option B:** From the Row Action tool for your work order type, select **Manage Departments**, then click **Add Department**

The **Department Details Wizard** has four pages:

### Page 1 — Basic Information
- **Code** and **Name** are required
- **Work Order Time Days** — if left blank or set to zero, ALMA defaults to 7 days
- **Printer** — select a printer if you want routing slips to print

Click **Next**.

### Page 2 — Library Association
- Verify your institution name is listed
- Optionally click **Attach Library** to associate a specific library within your institution

Click **Attach** if you selected a library, then **Next**.

### Page 3 — Contact Information *(optional)*
- Add addresses, phone numbers, and email addresses for the department
- Click **Add** in each section as needed

Click **Next**.

### Page 4 — Operators
- Add staff members who can process materials in this department
- Click **Add Operator** and search by name or use the list icon
- Click **Save**, then **Back**

Your work order is now complete.

---

## Step 4: Attach a Work Order Type to a Circulation Desk

Work orders must be attached to a circulation desk at the library level before they can be used.

1. Switch the Configuring menu to the **library** where the circulation desk is located.
2. Navigate to: **Fulfillment → Library Management → Circulation Desks**
3. Open the **Row Action** tool for the target circulation desk and select **Edit**.
4. Click the **Work Order Types** tab.
5. Click **Add Work Order** and select the work order type from the list.
6. Enter the **Work Order Time in Days**.
7. Click **Add Work Order**.
8. Click **Save**.

---

## Summary

Configuring work orders in ALMA involves defining types, adding statuses to each type, creating departments to handle the work, and attaching those types to circulation desks. This structure gives your library full visibility into where physical items are at every stage of an internal process — while keeping them available for patron requests throughout.
