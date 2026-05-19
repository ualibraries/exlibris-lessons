# ALMA Analytics: Running and Creating Reports

## Overview

ALMA Analytics allows you to answer important business questions and make data-driven decisions using reports, data visualizations, dashboards, and widgets — all of which can be shared with library staff.

Typical questions Analytics can answer include:
- What items have been overdue for at least 30 days?
- How much money do we pay to vendors?

In this tutorial, you will learn how to:
- Navigate the ALMA Analytics interface
- Run and customize an existing report
- Create a new report from scratch
- Save and share reports

---

## Accessing ALMA Analytics

Navigate to:

**ALMA → Analytics → Design Analytics**

> **Note:** You will need the **Design Analytics** role to access this area.

ALMA Analytics is built on **Oracle Analytics Server (OAS)**. The first time you enter, your dashboard will be empty — you can edit it and add any reports that interest you.

---

## Understanding the Data Refresh Cycle

Analytics data is updated through a daily **ETL (Extract, Transform, and Load)** process:

- **Data available as of** — the time the data completed the ETL process
- **Data updated as of** — the time the data was extracted from ALMA

> **Important:** Any activity that takes place in ALMA after the extract has started will **not** be reflected in the current data load. For this reason, it is recommended to schedule or run reports **early in the morning** rather than late at night.

---

## Navigating the Catalog

From the global header, go to **Catalog** to access existing reports. The folder structure is organized as follows:

| Folder | Contents |
|--------|----------|
| **My Folders** | Personal folder, accessible only to you |
| **Shared Folders → Alma** | Out-of-the-box reports created by Ex Libris (read-only) |
| **Shared Folders → [Your Institution]** | Reports accessible by users at your institution |
| **Shared Folders → Community** | Reports shared by other institutions |

---

## Running an Existing Report

### Example: Items Overdue for 30+ Days

1. In the Catalog, expand **Alma → Fulfillment → Reports**.
2. Locate the report named **Overdue Items**.
3. Click **Edit** — the report will run on your institution's data.
4. Go to the **Results** tab to see the output.

### Customizing the Report

The **Criteria** tab shows how the report was built, including its filters and selected columns. To narrow results to items overdue for more than 30 days:

1. Click the **gear icon** next to *Days Overdue*.
2. Select **Filter**.
3. Set the **Operator** to *Is Greater Than* and enter `30` in the value field.
4. Go to the **Results** tab to verify the filtered output.

### Saving a Customized Report

Because the Alma folder contains read-only reports, the **Save** button will be disabled. Instead:

1. Click **Save As**.
2. Change the location to: **Shared Folders → [Your Institution] → Reports**
3. Update the report name to accurately describe its content.
4. Click **OK**.

---

## Creating a New Report

### Example: Vendor Expenditure by Month

#### Step 1: Open a New Analysis

From the Catalog, click **New → Analysis**.

#### Step 2: Select a Subject Area

Analytics data is organized into subject areas. For financial information, select **Fund Expenditure**.

#### Step 3: Add Columns

Expand the subject area folders and double-click (or drag and drop) the fields you need into the **Selected Columns** area:

- Vendor Name
- Vendor Code
- Acquisition Method
- Transaction Amount *(a measure — Analytics calculates totals automatically)*
- Month and Year

#### Step 4: Apply Filters

To limit results to purchases only:
1. Click the **gear icon** next to *Acquisition Method* and select **Filter**.
2. In the Value dropdown, check **Purchase** and click **OK**.

To limit results to the current fiscal year:
1. Click the **gear icon** next to *Transaction Date Year* and select **Filter**.
2. Select the fiscal year you are reporting on and click **OK**.

#### Step 5: Remove Filter Columns from Display

Since Year and Acquisition Method are now filters rather than display columns, remove them from the results view:
1. Click the **gear icon** next to the column.
2. Select **Delete**.

#### Step 6: Add a Pivot Table View

To display the data organized by month:
1. Click the **New View** icon.
2. Select **Pivot Table**.

Scroll down to see the data reorganized by month. You can choose any alternative visualization to suit your needs.

#### Step 7: Save and Share the Report

- To save for personal use: save in **My Folders**.
- To share with colleagues: save under **Shared Folders → [Your Institution] → Reports**, add a name and description, and click **OK**.

---

## Summary

ALMA Analytics gives you powerful tools for answering real business questions using your library's data. By customizing existing out-of-the-box reports and building new analyses from subject areas, you can generate actionable insights and share them across your institution.
