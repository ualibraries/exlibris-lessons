# Alma Analytics: Exposing Reports to Staff via Analytics Objects

## Overview

Once you've created reports in Alma Analytics, you need to make them accessible to library staff. This is done through **Analytics Objects** — configurations that connect your reports to Alma's menus, dashboards, email subscriptions, and homepage widgets.

---

## Prerequisites

- You must have the **Analytics Administrator** role to access the Analytics Objects List and create objects.
- Reports should already exist in Design Analytics before creating objects for them.

---

## Accessing Analytics Objects

Navigate to **Analytics > Analytics Objects > Analytics Objects List**.

Click **Add New Analytics Object**, then choose **Add New Alma Analytics Object**.

---

## Types of Analytics Objects

| Object Type | How Users Access It |
|---|---|
| **Dashboard** | Analytics menu in Alma |
| **Data Visualization Project** | Analytics menu in Alma |
| **Report** | Analytics menu in Alma |
| **Scheduled Dashboard** | Email subscription (with file attachment) |
| **Scheduled Report** | Email subscription (with file attachment) |
| **Widget** | Alma homepage |

You can create more than one Analytics Object for the same underlying report.

---

## Creating a Report Analytics Object

### Step 1: Choose the Object Type

Select **Report** as the object type (Dashboard, Report, Data Visualization Project, and Widget share similar configuration parameters).

### Step 2: Enter Basic Information

- **Title** — A descriptive name for the Analytics Object; this is what users will see
- **Analytics Folder** — The location in Design Analytics where the original report resides
- **Analytics Report** — Select the specific report from that folder
- **Description** *(optional)* — Add context for users

### Step 3: Set Role-Based Access

Specify which user roles can view this Analytics Object:

1. Use **Add from Profiles** or **Add Role** to select roles
2. For example, an Acquisitions report might be visible to:
   - Acquisitions Administrator
   - User Administrator
3. Click **Add Role** to confirm each selection

### Step 4: Save

Click **Save**. The new object appears in the Analytics Objects List as a report.

---

## Managing Existing Analytics Objects

From the **Row Action** menu on the Analytics Objects List, you can:

- **View** the object
- **Edit** its configuration
- **Duplicate** it
- **Delete** it
- **Preview** the report in a pop-up window
- **View hidden columns**

> **Note:** To see a newly created report under the Reports menu immediately, you will need to **refresh** the page.

---

## Creating Scheduled Analytics Objects (Email Delivery)

If you choose **Scheduled Report** or **Scheduled Dashboard**, additional parameters are required:

| Parameter | Description |
|---|---|
| **Format** | File type attached to the email: PDF, Excel, Text, or CSV *(does not apply to dashboards)* |
| **Status** | Set to **Active** for the report to send on schedule |
| **Schedule** | Choose Daily, Weekly, or Monthly delivery |
| **FTP** *(optional)* | If sending to an FTP server, enter additional FTP configuration details |

For Scheduled Objects, the status (Active/Inactive) is visible in the Analytics Objects List. Staff can also **subscribe themselves** to a Scheduled Report from **Alma > Analytics > Subscribe to Analytics**.

---

## Widgets on the Alma Homepage

Users can add widget-type Analytics Objects directly to their Alma homepage:

1. Click the **+** (plus) icon on the Alma homepage
2. Check the desired widget object
3. Click **Refresh** — the widget will appear on the homepage

---

## Summary

| Goal | Path |
|---|---|
| Create an Analytics Object | Analytics > Analytics Objects > Analytics Objects List > Add New |
| Required role | Analytics Administrator |
| Expose report via menu | Create a Report-type object with appropriate roles |
| Deliver report by email | Create a Scheduled Report with format, status, and schedule |
| Add report to homepage | Create a Widget-type object; users add it via the + icon |
