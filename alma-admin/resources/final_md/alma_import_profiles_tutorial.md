# ALMA Import Profiles: A Setup Tutorial

## Overview

Import profiles are one of the primary ways to bring records into ALMA. They define the settings for how records from external sources will be imported, covering every step from ingestion to inventory creation.

The metadata import workflow includes the following stages, each of which must be configured:

1. **Data source** — where the records come from
2. **Indication, normalization, and validation** — filtering and correcting incoming data
3. **Match and merge** — identifying and handling duplicate records
4. **Set management tags** — applying tags to imported records
5. **Inventory operations** — creating physical or electronic inventory

This tutorial provides a high-level overview of each step. For detailed explanations of every parameter, refer to the *Managing Import Profiles* page in ALMA Online Help.

---

## Accessing Import Profiles

Navigate to:

**ALMA → Resources → Import → Manage Import Profiles**

This page displays the status, name, description, and type of each existing import profile.

---

## Creating a New Import Profile

Click **Add New Profile** to begin. You will be presented with a list of profile types, each with a brief description. Common types include:

- **Repository** — loads bibliographic records; can create physical and/or electronic inventory based on configured parameters
- **New Order** — loads bib records with embedded order data; creates PO lines and inventory

This tutorial uses the **Repository** profile type as its example. Select **Repository** and click **Next**.

---

## Step 1 of 6 — Profile Details

*Note: The wizard begins on Step 2 after selecting a profile type.*

On this screen, configure the basic profile information:

- **Name and Description** — be as specific as possible so you can easily identify when this profile should be used
- **Source of Records** — select where the records are coming from (e.g., Library of Congress)
- **Import Protocol**:
  - **FTP** — allows you to schedule the import to run at set intervals; configure FTP details as needed
  - **Manual Upload** — records are uploaded manually each time
- **Physical Source Format** — e.g., XML
- **Source Format** — e.g., MARC 21 Bibliographic
- **Target Format** — e.g., MARC 21 Bibliographic
- **Status** — set to **Active** for the profile to appear as an option when running an import job

Click **Next** to proceed.

---

## Step 2 of 6 — Indication, Normalization, and Validation

This step allows you to filter and clean incoming records before they are imported.

### Indication Rules
Set up filters on your records based on indication rules to control which records are processed.

### Normalization
Use normalization rules to correct incoming data. For example:
- If incoming records contain fields that do not apply to your institution (e.g., 029 fields), you can configure a normalization rule to delete them during import.

Under **Normalization**, select **Correct the data using** and choose the appropriate normalization rule.

### Validation Exception Profile
Determines how ALMA handles records that did not import correctly. Choose a profile that reflects how strictly you want import errors to be enforced.

> You can add your own indication rules, normalization processes, and validation rules. For details, refer to ALMA Online Help.

Click **Next** to proceed.

---

## Step 3 of 6 — Match and Merge

This step configures how ALMA identifies duplicate records and what to do when a match is found.

### Match Profiles

Select a **match method** appropriate for your record type. Options are available for both serial and non-serial records. Examples:
- **ISSN 024035** — for serials
- **ISBN 024035** — for non-serials importing brand new records

> For specifics on each match method, see the *Managing Import Profiles* page in ALMA Online Help.

### Match Actions

If ALMA detects that an incoming record matches an existing record, the match action determines how it responds:

| Handling Method | Behavior |
|-----------------|----------|
| **Manual** | Requires you to resolve each match manually |
| **Automatic** | Resolves matches based on your configured upon-match behavior |

**Upon Match** options include:
- Merge or overlay the existing record
- Do not import the incoming record
- Import the incoming record as a new record

### Additional Match Options

- **Consider Inventory Type** — if checked, records with different inventory types will not be considered a match
- **Merge Method** — determines how fields are handled when merging (e.g., *Overlay All Fields But Local*). Merge methods are created in the Metadata Editor.
- **Match Action Options** — can prevent low-quality records from overlaying good-quality records, and can prevent the import process from overriding the originating system

### Automatic Multi-Match Handling

When **Automatic** is selected as the handling method, this section becomes available. Options work **hierarchically** — only selected options are considered.

- **Merge Records and Combine Inventory for Multi-Match** — merges two or more existing duplicate records into one before merging or overlaying with the incoming record
- **Disabled** — ignores this section entirely

### No Match Found

If no matching record is found, select either:
- **Do Not Import**
- **Import** (as a new record)

Click **Next** to proceed.

---

## Step 4 of 6 — Set Management Tags

Apply tags to all records imported using this profile. For each tag, you can set the condition:
- **Only for new records**
- **Unconditionally** (applies to all imported records)

Available tags include settings for:
- **Suppress from Discovery** — whether records are hidden from patron-facing discovery
- **Suppress from External Search** — whether records are hidden from external search
- **Automatic Synchronization** — e.g., synchronize with OCLC or Libraries Australia

Click **Next** to proceed.

---

## Step 5 of 6 — Inventory Operations

Choose whether to create inventory from the imported records, and if so, what type.

### Electronic Resources

If importing electronic resource records:

1. Enter **general information** — e.g., whether to delete existing portfolios, material type
2. **Map fields and subfields** — identify where portfolio information is found in the incoming data, including:
   - Portfolio URL
   - Description
   - Library
3. Choose whether to **automatically activate** the resource upon import

### Physical Resources

If importing physical records:

1. Choose whether to create:
   - **Items and Holdings**
   - **Holdings Only**
2. Select the **material type** (e.g., Book)
3. Select the **field** from which to map item information (e.g., field 905 — the field column for all parameters will be automatically populated)
4. Indicate where each detail exists in the file. **Default values** entered here will be used if a field is blank or contains an incorrect value in the input file.

### Holdings Mapping

Use **Add Holdings Mapping** to map fields from the imported bibliographic record to fields in the new holdings record in ALMA.

> Note: There is no need to map 852 subfield B or subfield C — these fields are already mapped automatically.

- **Update Holdings Call Number** — when enabled, updates the holdings record with a call number from the imported bibliographic record

---

## Saving and Activating Your Profile

At any step in the wizard, you can click **Save Draft**. The profile will be saved as **inactive**.

To find and activate a saved draft:

1. Search for the profile (e.g., by description).
2. Click **Edit** — the wizard steps will now display as tabs.
3. Go to the **Profile Details** tab and change the status to **Active**.
4. Click **Save**.

The profile is now ready to use for importing records.

---

## Summary

Import profiles give you full control over how external records enter ALMA — from the source and format of the data, through normalization and deduplication, to the creation of physical or electronic inventory. Configuring each step carefully ensures that imported records meet your institution's quality standards and are ready for immediate use.
