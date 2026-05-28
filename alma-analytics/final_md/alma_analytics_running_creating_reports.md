# Alma Analytics: Running and Creating Reports

## Overview

Alma Analytics allows you to answer important business questions using reports, data visualizations, dashboards, and widgets — enabling data-based decisions across your library. This tutorial walks through two common use cases:

1. Finding items overdue for at least 30 days using an existing report
2. Creating a new report to track vendor expenditures

---

## Understanding the Analytics Environment

### Accessing Design Analytics

Navigate to **Analytics > Design Analytics**. You will need the **Design Analytics role** to enter this area.

Alma Analytics is built on **Oracle Analytics Server (OAS)**, which is the interface used for building and managing reports.

### Data Refresh Schedule

Every day, a full database refresh takes place through an **ETL (Extract, Transform, Load)** process:

- **Data available as of** — the time the ETL process completed
- **Data updated as of** — the time data was extracted from Alma

> **Tip:** Any Alma activity that occurs *after* the extract has started will not appear in the current data load. Run or schedule reports **early in the morning** rather than late at night.

### Navigating the Catalog

From Design Analytics, go to **Catalog** to access reports:

- **My Folders** — Personal folder, visible only to the logged-in user
- **Shared Folders > Alma** — Out-of-the-box reports created by Ex Libris (read-only)
- **Shared Folders > [Your Institution]** — Reports accessible to users at your institution
- **Community** — Reports shared by other institutions

---

## Tutorial 1: Finding Items Overdue 30+ Days (Using an Existing Report)

### Step 1: Locate the Report

1. Go to **Catalog**
2. Expand **Alma > Fulfillment > Reports**
3. Find the report named **Overdue Items**
4. Click **Edit** to run it on your institution's data

### Step 2: Review the Report Structure

Under the **Criteria** tab, you can see how the report is written:

- **Filters:** Active loans with a due date before today, from the past year, filtered by library and circulation desk
- **Selected Columns:** Library name, title, barcode, days overdue, and more

### Step 3: Add a Custom Filter

To narrow results to only items overdue by more than 30 days:

1. Click the **gear icon** next to **Days Overdue**
2. Choose **Filter**
3. Set the **Operator** to **Is Greater Than**
4. Enter `30` in the value field
5. Click **OK** — the new filter appears in the Filters section
6. Click the **Results** tab to view the filtered list

### Step 4: Save the Report

Because the Alma folder is read-only, the **Save** button will be disabled. Instead:

1. Choose **Save As**
2. Change the location to **Shared Folders > [Your Institution] > Reports**
3. Update the report name to accurately describe it
4. Click **OK**

Your report is now saved and ready to share with library staff.

---

## Tutorial 2: Creating a Vendor Expenditure Report (New Report)

### Step 1: Create a New Analysis

1. From **Catalog**, click the **New** icon and select **Analysis**
2. Choose the subject area: **Fund Expenditure**

> Analytics data is organized into subject areas. Financial transaction data lives under **Fund Expenditure**.

### Step 2: Select Your Columns

Expand the available folders and double-click (or drag-and-drop) the following fields into the **Selected Columns** area:

- Vendor Name
- Vendor Code
- Acquisition Method
- **Transaction Amount** *(this is a measure — Analytics calculates totals automatically)*
- Month and Year

### Step 3: Apply Filters

**Filter by Acquisition Method (Purchases only):**

1. Click the **gear icon** next to **Acquisition Method**
2. Choose **Filter**
3. In the Value dropdown, check **Purchase**
4. Click **OK**

**Filter by Current Fiscal Year:**

1. Click the **gear icon** next to **Transaction Date Year**
2. Choose **Filter**
3. Select the fiscal year you are reporting on
4. Click **OK**

### Step 4: Clean Up the Columns

Since Acquisition Method and Year are now filter-only fields (not needed as display columns):

1. Click the **gear icon** next to **Acquisition Method**
2. Choose **Delete**
3. Repeat for the Year column

### Step 5: Review and Visualize

1. Click the **Results** tab to see your vendor list with amounts
2. To view data by month, click the **New View** icon and select **Pivot Table**
3. Scroll down to see amounts organized by month
4. You can choose any alternative visualization type to suit your needs

### Step 6: Save the Report

- To save for personal use: save to **My Folders**
- To share with colleagues: save to **Shared Folders > [Your Institution] > Reports**
  1. Fill in a name and optional description
  2. Click **OK**

Your report is now ready for others to view.

---

## Summary

| Task | Where to Start |
|---|---|
| Access Analytics | Analytics > Design Analytics |
| Find existing reports | Catalog > Alma or [Institution] folder |
| Create a new report | Catalog > New > Analysis |
| Save a shared report | Shared Folders > [Institution] > Reports |
| Schedule or run reports | Early morning recommended |
