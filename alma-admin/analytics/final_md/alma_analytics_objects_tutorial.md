# ALMA Analytics Objects: Sharing Reports with Staff

## Overview

Once you have created reports in ALMA Analytics, the next step is making them accessible to library staff. This is done by creating **Analytics Objects** — wrappers that expose Analytics reports to users based on their roles, without requiring them to access Design Analytics directly.

In this tutorial, you will learn how to:
- Understand the different types of Analytics Objects
- Create an Analytics Object and assign user roles
- Configure scheduled reports and dashboards
- Access Analytics Objects as an end user

---

## Accessing Analytics Objects

Navigate to:

**ALMA → Analytics → Analytics Objects → Analytics Objects List**

> **Note:** You will need the **Analytics Administrator** role to access the Analytics Objects List page and create objects.

Click **Add New Analytics Object → Add New Alma Analytics Object** to begin.

---

## Types of Analytics Objects

Different object types determine how users access and receive reports:

| Object Type | How Users Access It |
|-------------|---------------------|
| **Dashboard** | Available from the Analytics menu in ALMA |
| **Data Visualization Project** | Available from the Analytics menu in ALMA |
| **Report** | Available from the Analytics menu in ALMA |
| **Scheduled Dashboard** | Delivered by email as an attachment on a recurring schedule |
| **Scheduled Report** | Delivered by email as an attachment on a recurring schedule |
| **Widget** | Displayed on the ALMA homepage |

You can create more than one object type for the same Analytics report.

---

## Creating an Analytics Object

The following steps use **Report** as the object type example. Dashboard, Data Visualization Project, and Widget follow a similar process.

### Step 1: Enter Basic Information

- **Title** — enter a descriptive name that will be meaningful to end users
- **Analytics Folder** — select the location in Design Analytics where the original report resides
- **Name** — select the specific Analytics report from the folder

You can also add an optional **description**.

### Step 2: Assign User Roles

Use **Add from Profiles** or **Add Role** to specify which user roles can view this Analytics Object. Only users with the assigned roles will see the object.

**Example:** For an Acquisitions Report, you might assign:
- Acquisition Administrator
- User Administrator

Click **Add Role** to save each selection.

### Step 3: Save

Click **Save**. The new object appears in the Analytics Objects List as a report.

---

## Managing Analytics Objects

From the **Row Actions** list next to any object, you can:
- **View** — open the object
- **Edit** — modify its settings
- **Duplicate** — copy it as a starting point for a new object
- **Delete** — remove it
- **Preview** — view the report in a pop-up window
- **View Hidden Columns** — inspect columns that are not displayed in the report output

---

## Configuring Scheduled Reports and Dashboards

If you are creating a **Scheduled Report** or **Scheduled Dashboard**, additional parameters must be filled in, as these objects deliver reports by email via a periodically running job:

| Parameter | Description |
|-----------|-------------|
| **Format** | File type attached to the email: PDF, Excel, Text, or CSV *(does not apply to dashboards)* |
| **Status** | Set to **Active** for the report to be sent on schedule |
| **Schedule** | Choose **Daily**, **Weekly**, or **Monthly** delivery |
| **FTP** | If sending to an FTP server, enter additional FTP configuration details |

> For more information on FTP report scheduling, see the *Scheduling and Subscribing to Alma Analytics Reports* page in ALMA Online Help.

---

## How Users Access Analytics Objects

Depending on the object type, users with the appropriate role can access objects in the following ways:

### Reports, Dashboards, and Data Visualization Projects
Users can run these from:

**ALMA → Analytics → Reports**

> **Note:** To see a newly created object under the Reports menu, users may need to **refresh** the page.

### Scheduled Reports and Dashboards
- Administrators can see the **Active** status of scheduled objects from the Analytics Objects List.
- Users can **subscribe** to scheduled report mailing lists from:

  **ALMA → Analytics → Subscribe to Analytics**

### Widgets
Users can add widgets to their ALMA homepage:
1. Click the **+ (plus) icon** on the ALMA homepage.
2. Check the desired widget object.
3. Refresh the page — the widget will now appear on the homepage.

---

## Summary

Analytics Objects are the bridge between the reports you build in Design Analytics and the staff who need to act on that data. By creating objects, assigning roles, and optionally scheduling delivery, you can ensure the right people have access to the right information — without requiring everyone to access the Analytics design environment directly.
