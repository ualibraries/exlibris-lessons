# ALMA Metadata Profiles: Configuration and Validation Tutorial

## Overview

Metadata profiles — such as MARC 21 Bibliographic or Dublin Core — are schemas with defined sets of attributes used to describe physical, electronic, and digital materials. When you open a MARC 21 Bibliographic record in ALMA, the fields and subfields you see are defined by these metadata profiles.

In this tutorial, you will learn how to:
- Configure metadata profiles
- Edit fields and subfields within the MARC 21 profile
- Set up normalization processes
- Configure validation rules and exception profiles

---

## Accessing Metadata Configuration

Navigate to:

**ALMA Configuration → Resources → Cataloging → Metadata Configuration**

The profiles displayed here are the active profiles your library can configure. The available profiles are determined by Ex Libris.

---

## Opening a Metadata Profile

Click on a profile name (e.g., **MARC 21 Bibliographic**) to open the **Profile Details** page.

> **Note:** The tabs and parameters shown may differ between profiles.

The Profile Details page contains several tabs:
- **Fields** — metadata fields for the profile
- **Forms** — templates for creating digital representations
- **Normalization Processes** — rules to correct or update records
- **Validation Processes** — out-of-the-box validation rules
- **Validation Exception Profile List** — severity settings for validation issues
- **Other Settings** — brief level rules and record-saving behavior

---

## Configuring Fields

### Navigating the Fields Tab

The **Fields** tab displays all metadata fields for the profile. When the filter is set to **All**, the complete list appears. You can:
- Use the **filter options** to navigate to a specific area of the schema
- Use the **field search box** to search by field number or description

### Editing a Field

1. Locate the field you want to edit (e.g., field **310**).
2. Click the **Row Actions** button to see available options:
   - **View** — read-only view of the field
   - **Edit** — open the field for editing
   - **Restore** — return the field to its default settings (available if the field has been customized)
3. Select **Edit** to open the **Field Details** page.

On the Field Details page, you can:
- Set whether the field is **mandatory**
- Change the **description**
- Add a **help URL** — the linked content appears in the field information area of the Metadata Editor. If left blank, ALMA defaults to the Library of Congress cataloging standard information.

### Configuring Subfields

From the Field Details page, scroll to the subfields list. For each subfield you can:
- Edit the **description**
- Set the subfield as **mandatory**
- Determine whether it is **repeatable**
- Assign a **controlled vocabulary** via the row action list

#### Assigning a Controlled Vocabulary

A controlled vocabulary is a list of acceptable values for a subfield. To assign one (e.g., to subfield A):

1. From the row action list, select the option to assign a controlled vocabulary.
2. Choose one of the following:
   - **Select an existing controlled vocabulary** from the dropdown list — details will display on screen.
   - **Create a new local controlled vocabulary** — enter a code, a description, and click **Add**. This will apply only to this specific field.
3. Click **Assign** to save your changes.

> For more information, see the *Configuring Controlled Vocabulary Registry* page in ALMA Online Help.

### Configuring Indicators

After configuring subfields, expand the **First Indicator** and **Second Indicator** sections on the Field Details page, make any required changes, and click **Save**.

---

## Configuring Forms

Under the **Forms** tab, you can create a form consisting of a template of fields to be used when creating digital representations.

> For full details, see the *Configuring Cataloging* page in ALMA Online Help.

---

## Configuring Normalization Processes

The **Normalization Processes** tab lists processes that correct or update records. These processes apply to the entire MARC 21 Bibliographic profile.

### Adding a New Normalization Process

Click **Add Process** to create a new normalization process associated with this metadata profile.

### Editing an Existing Process

1. From the row action list next to an existing process, select **Edit** (you can also **Copy** or **Delete**).
2. The **Task List** tab displays all tasks this process will perform.
3. Click **Add Tasks** to add a task from a predefined list, or remove an existing one.

#### Using an Existing Normalization Rule

To run a normalization rule from the Metadata Editor:
1. Choose **Marked Rule Normalization Task**.
2. In the **Task Parameters**, select the normalization rule you want to run.
3. Click **Save**.

> For detailed information about available tasks, see the *Configuring Metadata* page in ALMA Online Help.

---

## Configuring Validation Processes

The **Validation Processes** tab displays the out-of-the-box validation processes, each handling different record types. You can **edit** these processes but cannot create new ones.

### Editing a Validation Process

1. Select a process to open the **Process Details** page.
2. Go to the **Task List** tab to view the tasks this process performs.
   - For example, the **Validation Repeatable MARC 21** task validates repeatable and non-repeatable fields according to your configuration in the Fields tab.
3. Add or remove tasks as needed.

> For details on what each task validates, see the *Configuring Cataloging* page in ALMA Online Help.

---

## Configuring Validation Exception Profiles

The **Validation Exception Profile List** tab lets you define the severity of validation issues. When ALMA encounters an issue from a validation process, you determine whether it results in:

- **Error** — blocks the user from continuing until the issue is resolved
- **Warning** — alerts the user but allows them to proceed

### Understanding the Profile List

The tab displays the name, description, and default severity of each profile. Two profiles are provided out-of-the-box.

### Editing a Validation Exception Profile

Using the **MARC XML Bib Metadata Editing on Save** profile as an example (default severity: Warning):

1. Click **Edit** to open the profile.
2. Under **General Information**, view or change the default behavior for all validation issues.
3. The table below shows **exceptions** — specific issues that will trigger an error and block the user until resolved.
   - Example: If a record is missing the mandatory field **245**, ALMA will present an error and block the user from saving until a value is entered.

### Adding a Validation Severity Exception

1. Click **Add Validation Severity Exception**.
2. Select the **message** to be displayed.
3. Fill in the required parameters (e.g., for *Mandatory Subfield is Missing in Field*, specify the subfield and field).
4. Click **Add Validation Severity Exception** to save.

---

## Other Settings

The **Other Settings** tab allows you to:
- Select a **brief level rule** for the profile
- Set **parameters** for handling certain fields in a particular way when saving records

---

## Summary

Configuring ALMA's metadata profiles gives you precise control over how records are structured, validated, and normalized. By customizing fields, assigning controlled vocabularies, defining normalization processes, and setting validation severity levels, you can ensure that cataloging at your institution meets your standards consistently.
