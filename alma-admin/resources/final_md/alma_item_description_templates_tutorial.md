# ALMA Item Description Templates and Sort Routines: A Configuration Tutorial

## Overview

When catalogers receive physical items — typically serials and subscription monographs — they generate **item descriptions** that allow ALMA to treat each issue as a unique copy. These descriptions are built automatically using **description template rules**, which format information such as volume, issue number, year, and month into a consistent, readable string.

In this tutorial, you will learn how to:
- Configure a description template rule to generate and format item descriptions
- Update item descriptions in bulk using a job
- Sort physical items by description using sort routines

---

## Accessing Description Templates

Navigate to:

**ALMA Configuration → Resources → General → Description Templates**

The **Institution Rules** list displays all template rules available at your institution. ALMA runs these rules **from top to bottom**, in the order they appear. If no rule applies to a given item, ALMA falls back to the **default rule**.

To change the order in which rules are evaluated, use the **Move Up** and **Move Down** arrows.

---

## Creating a Description Template Rule

You can create a new rule two ways:
- Click **Add Rule** to start from a blank form
- Select **Duplicate** from the Row Actions list of an existing rule to copy and modify it

### Step 1: Enter Template Name and Description

On the **Description Template Setup** page:
- Enter a **Template Name** that clearly reflects what the template produces (e.g., *Volume, Number, Year, Month*)
- Enter a **Description** showing how the output will look (e.g., *volume.number (year month)*)

### Step 2: Configure Input Parameters

Input parameters define which items this rule applies to. Click **Add Parameter** to add one or more conditions. Examples include:
- Items in a certain library
- Items with specific fields present

To target items containing the fields you need:
1. Choose **Material Type** from the parameter options.
2. Select **Issue** from the list.
3. Add any additional parameters for the data fields required.

> A rule will only apply to items that match **all** input parameters you define.

### Step 3: Configure Output Parameters

Output parameters define what information appears in the generated description and how it is formatted. For each field you want to display:

1. Specify the **field name** from the item record (ALMA will populate this field with the value entered in the New Item Details screen at receiving time)
2. Enter a **prefix** (text that appears before the value)
3. Enter a **suffix** (text that appears after the value)

#### Example: Volume, Number, Year, Month

| Display Element | Item Record Field | Example Prefix | Example Suffix |
|----------------|-------------------|----------------|----------------|
| Volume | Enumeration A | `v.` | *(none)* |
| Issue Number | Enumeration B | `no.` | *(none)* |
| Year | Chronology I | `(` | *(none)* |
| Month | Chronology J | *(none)* | `)` |

> **Important:** All fields chosen in the output parameters must be present in the item record for the description to be correctly formatted. For a full list of available fields and parameters, see the *Receiving Physical Material* article in ALMA Online Help.

### Step 4: Preview and Save

- Click **Show Template** to preview how the generated description will look.
- If the result is correct, click **Save**.

To edit or delete a rule later, use the **Row Actions** list next to any rule in the Institution Rules list.

---

## Updating Item Descriptions in Bulk

If you edit an existing template rule and want to retroactively apply it to already-received items, you can rebuild descriptions in bulk using a job.

### Steps

1. **Create a set** of the item records you want to update.
2. Navigate to: **ALMA → Admin → Manage Jobs and Sets → Run a Job**
3. Search for **Description** and select **Rebuild Physical Item Description**.
4. Click **Next**.
5. Select the set you created and click **Next**.
6. Click **Submit** and confirm.

### Monitoring the Job

- Click **Refresh** to check the job's progress.
- When complete, the job will appear on the **History** tab with a status of *Completed*.

---

## Configuring Physical Item Sort Routines

Once item descriptions are generated, you can use them to control how physical items are sorted and displayed throughout ALMA — for example, in the Receiving Workbench or Item Editor.

### Accessing Sort Routines

Navigate to:

**ALMA Configuration → Resources → General → Physical Items Sort Routines**

Existing sort routines are listed here. Click **Add Sort Routine** to create a new one.

### Creating a Sort Routine

1. Enter a **Name** and **Description** for the routine.
2. Select the **sort order**:
   - **Ascending**
   - **Descending**
3. Choose the **field or fields** by which to sort (e.g., *Description*).
4. Click **Add to Selection**.
5. Click **Next**.

### Assigning the Sort Routine to ALMA Areas

Select the areas of ALMA where you want this sort routine to be available. For example:
- **Receiving Workbench**
- **Item Editor**

For each area, you can optionally set the routine as the **default sort** for items displayed there.

Click **Save** when done.

### Verifying the Sort Routine

When searching for physical titles and viewing their items in ALMA, the new sort routine will appear in the sort options and — if set as default — will be applied automatically.

---

## Summary

Description template rules give you precise control over how ALMA generates item descriptions for serials and subscription monographs at receiving time. Combined with the Rebuild Physical Item Description job for retroactive updates and sort routines for consistent display ordering, these tools help maintain an organized and browsable physical collection.
