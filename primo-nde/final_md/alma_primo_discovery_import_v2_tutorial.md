# Primo VE Discovery Import Profiles: A Tutorial

## Overview

Primo VE allows you to import records from external sources — in **Generic XML**, **Dublin Core**, or **MARC 21** formats — so patrons can find them in your local catalog.

> **Important:** Records loaded through Discovery Import Profiles are stored directly in Primo VE. They **cannot** be searched or viewed using ALMA's repository search — they are only accessible through Discovery.

The import process has three stages:

1. **Normalization Rules** — transform and enrich source data for use in Primo VE
2. **Normalization Process Task** — group normalization rules into a reusable process
3. **Discovery Import Profile** — define the external source, apply normalization, configure delivery links, and schedule execution

---

## Stage 1: Create or Review Normalization Rules

Normalization rules copy and transform data from source records into Primo VE fields, enabling resource type mapping and improved search/facet behavior.

> Depending on your source data, this step may not be needed.

### Accessing Normalization Rules

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Normalization Rules for External Data Sources**

This opens the Metadata Editor.

- Check under **Normalization → Discovery** for existing rules that can be modified or reused.
- To test a rule, click **Save and Test Using External Record** (use a sample record from your external source, not from ALMA).

> Only rules saved in the **Shared** folder can be assigned to normalization process tasks. Private rule files cannot be used.

---

## Stage 2: Create a Normalization Process Task

A normalization process task groups normalization rule files so they can be assigned to import profiles.

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Normalization Process Task**

### Step 1 — Business Entity and Type

1. Click **Add Process**.
2. Select the **Business Entity**:
   - *Discovery Bib Records* — for Dublin Core and Generic XML sources
   - *Bibliographic Title* — for MARC 21 sources
3. Select the **Type** (format of the normalization rules):
   - Example: *Discovery Generic XML Normalization* for XML sources
4. Click **Next**.

### Step 2 — Name and Status

1. Enter a **Name** and **Description** (both required — indicated by red asterisks).
2. Set **Status** (active or inactive upon completion).
3. Click **Next**.

### Step 3 — Add Tasks

1. Click **Add Tasks**.
2. Check the box(es) for the task(s) to include.
3. Click **Add** to continue adding, or **Add and Close** when finished.
4. To remove a task: Row Action tool → **Remove**.
5. Click **Next**.

### Step 4 — Select Normalization Rule File

Select the **shared normalization rule file** to run. Private files cannot be added here.

Click **Save**. Use the **toggle** to activate the process when ready.

From the Row Action tool you can also **View**, **Edit**, **Copy**, or **Delete** the process.

---

## Stage 3: Create a Discovery Import Profile

Navigate to:

**ALMA Configuration → Discovery → Loading External Data Sources → Discovery Import Profiles**

*(Also accessible from the main ALMA dashboard.)*

The page lists all import profiles at your institution, plus network and community profiles.

> The **Network tab** is only visible for consortia environments.

### Step 1 — Profile Details

Click **Add New Profile**, confirm **Discovery** is selected, and click **Next**.

Required fields:
- **Profile Name**
- **Data Source Code**
- **Data Source Label**
- **Originating System**

For **Generic XML** sources, also configure:
- **Source Format**: XML
- **File Splitter Parameters** (required):
  - Root element tag
  - Record elements tag
  - XPath to the identifier tag

Click **Next**.

### Step 2 — (Internal processing step)

### Step 3 — Normalization Process

Select the normalization process task created in Stage 2. Click **Next**.

### Step 4 — Delivery Configuration

Define how records link to resources. Three link types are available:

| Link Type | Where It Appears in Full Record | Brief Results Display |
|-----------|--------------------------------|----------------------|
| **Link to Resource** | View It section | *Available Online*; included in Available Online facet |
| **Link to Request** | Links section | *Check Holding Status*; included in Held by Library facet |
| **Link to Thumbnail** | Record display | Resource type thumbnail images |

For each link type, choose a linking method:

**Static URL from Source:**
- Select the Dublin Core tag type
- Enter the standard link label used for all records
- Best when data consistently contains a link in one field

**Template (recommended when data is inconsistent):**
- Enter a **Linking Parameter** reference and link label
- Scroll to the **Linking Parameters** section to define each parameter

#### Configuring a Linking Parameter

1. Open the Row Action tool for Linking Parameter 1 → **Edit**.
2. Select the **Source Tag** (e.g., *dcterms:identifier*).
3. Set the condition for when to use this tag:
   - Select **Matching String using a regular expression**
   - Enter a regex that identifies the field (e.g., to match URLs starting with `http`)
4. Click **Save**.

Repeat for any additional linking parameters.

Click **Save** when the profile is complete.

---

## Running the Import Profile

1. From the import profiles list, open the Row Action tool → **Run**.
2. Upload your data file when prompted.
3. Click **Submit**.
4. You are taken to the **Job History** screen — click **Refresh** to monitor progress.
5. When complete, status shows *Completed Successfully*.

---

## Deleting Records Loaded via Discovery Import

Navigate to:

**ALMA → Admin → Manage Jobs and Sets → Run a Job**

1. Filter the job type to **Discovery Management**.
2. Select **Delete External Data Sources** and click **Next**.
3. In the **Data Source** drop-down, select the import profile used to load the records.
   - If multiple profiles were used, choose the **last one used**.
4. Click **Next**, confirm the data source information, and click **Submit**.

The records from the selected import profile will be removed from Primo VE.

---

## Summary

Discovery Import Profiles provide a structured, repeatable process for loading external records into Primo VE. Building normalization rules and process tasks ensures imported records are properly formatted for search and discovery. Once records are loaded, they are fully manageable — including deletion — through standard ALMA job workflows.
