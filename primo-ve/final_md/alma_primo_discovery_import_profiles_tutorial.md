# Primo VE Discovery Import Profiles: A Tutorial

## Overview

Primo VE allows you to import records from external sources — in **Generic XML**, **Dublin Core**, or **MARC 21** formats — so patrons can find them in your local catalog.

> **Important:** Records loaded through Discovery Import Profiles are stored directly in Primo VE. They **cannot** be searched or viewed using ALMA's repository search — they are only discoverable through Primo VE.

The import process involves three stages:

1. **Normalization Rules** — transform and enrich the source data for use in Primo VE
2. **Normalization Process Task** — group normalization rules into a process that can be assigned to an import profile
3. **Discovery Import Profile** — define the external data source, apply normalization, configure delivery links, and schedule the job

---

## Stage 1: Create Normalization Rules

Normalization rules copy and transform data from source records into Primo VE fields (using expanded Dublin Core or MARC 21 schema), enabling resource type mapping and other enhancements.

> Depending on your data, this step may not be needed.

### Accessing Normalization Rules

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Normalization Rules for External Data Sources**

This opens the Metadata Editor on the Rules tab.

- Check under **Normalization → Discovery** for any existing rules that can be modified or used as a starting point.
- If you make changes or create new rules, click **Save and Test Using External Record** to test against a sample record from your external source (not an ALMA record).

> Only rules saved in the **Shared** folder will be available to assign to normalization process tasks.

---

## Stage 2: Create a Normalization Process Task

A normalization process task groups normalization rule files together so they can be assigned to import profiles.

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Normalization Process Task**

Existing tasks are listed here. To create a new one:

### Step 1 — Business Entity and Type

1. Click **Add Process**.
2. Select the **Business Entity**:
   - *Discovery Bib Records* — for Dublin Core and Generic XML sources
   - *Bibliographic Title* — for MARC 21 sources
3. Select the **Type** (the format of the normalization rules):
   - Example: *Discovery Generic XML Normalization* for XML data sources
4. Click **Next**.

### Step 2 — Name and Status

1. Enter a **Name** and **Description** (both required, indicated by red asterisks).
2. Set the **Status** (active or inactive upon completion).
3. Click **Next**.

### Step 3 — Add Tasks

1. Click **Add Tasks**.
2. Check the box(es) for the task(s) to include.
3. Click **Add** to continue adding tasks, or **Add and Close** when finished.
4. To remove a task, use the Row Action tool → **Remove**.
5. Click **Next**.

### Step 4 — Select Normalization Rule File

Select the **shared normalization rule file** to run. Private files cannot be added here.

Click **Save**. Use the **toggle** to activate the process when ready.

From the Row Action tool, you can also **View**, **Edit**, **Copy**, or **Delete** the process.

---

## Stage 3: Create a Discovery Import Profile

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Discovery Import Profiles**

*(Also accessible from the main ALMA dashboard: Discovery → Loading External Data Sources → Discovery Import Profiles)*

This page lists all import profiles configured at your institution, as well as network and community profiles.

> The **Network tab** is only visible if you are part of a consortia environment.

### Step 1 — Profile Details

Click **Add New Profile**, confirm **Discovery** is selected, and click **Next**.

Required fields:
- **Profile Name**
- **Data Source Code**
- **Data Source Label**
- **Originating System**

For **Generic XML** sources, also set:
- **Source Format**: XML
- **File Splitter Parameters** (required for XML):
  - Root element tag
  - Record elements tag
  - XPath to the identifier tag

Click **Next**.

### Step 2 — (Not shown in wizard)

### Step 3 — Normalization Process

Select the normalization process task you created. Click **Next**.

### Step 4 — Delivery Configuration

Define how records link to resources. Three link types are available:

| Link Type | Where It Appears | Brief Results Behavior |
|-----------|-----------------|----------------------|
| **Link to Resource** | View It section | Displays as *Available Online*; included in the Available Online facet |
| **Link to Request** | Links section | Displays *Check Holding Status*; included in the Held by Library facet |
| **Link to Thumbnail** | Record display | Shows thumbnail images for resource types |

For each link type, choose between:
- **Static URL from Source** — use a consistent Dublin Core tag field for all records
- **Template** — build a dynamic link using linking parameters (useful when data is inconsistent)

#### Configuring a Linking Parameter (Template Method)

1. In the Link to Resource section, enter **Linking Parameter 1** as the template reference and provide a **link label**.
2. Scroll to the **Linking Parameters** section.
3. Open the Row Action tool for Linking Parameter 1 → **Edit**.
4. Select the **Source Tag** (e.g., *DC Terms → Identifier*).
5. Select when to use the source tag — for example, **Matching String using a regular expression** to only use identifiers that start with `http`.
6. Click **Save**.

Repeat for any additional linking parameters needed.

Click **Save** when the profile is complete.

---

## Running a Discovery Import Profile

1. From the import profiles list, open the Row Action tool → **Run**.
2. Upload your data file when prompted.
3. Click **Submit**.
4. You are taken to the **Job History** screen — click **Refresh** to monitor progress.

---

## Deleting Records Loaded via Discovery Import

Navigate to:

**ALMA → Admin → Manage Jobs and Sets → Run a Job**

1. Filter the job type to **Discovery Management**.
2. Select **Delete External Data Sources** and click **Next**.
3. In the **Data Source** drop-down, select the import profile used to load the records.
   - If multiple profiles were used to import the same records, choose the **last one used**.
4. Click **Next**, confirm the data source information, and click **Submit**.

The records from the selected import profile will be removed from Primo VE.

---

## Summary

Discovery Import Profiles give you a structured, repeatable process for loading external records into Primo VE. By building normalization rules to enrich the data, grouping them into process tasks, and configuring delivery links in the import profile, you ensure that externally sourced records are discoverable and actionable for your patrons — and removable when no longer needed.
