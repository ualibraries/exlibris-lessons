# ALMA Call Number Mapping Table: A Customization Tutorial

## Overview

When a new holdings record is created, ALMA uses the **call number mapping table** to automatically copy the call number from the bibliographic record into the holdings record. The table comes with predefined rules that work for the typical needs of many institutions — but you can also customize it as needed.

In this tutorial, you will learn how to:
- Understand and customize the call number mapping table
- Create a holdings template that automatically populates with the correct call number

---

## Finding the Call Number Mapping Table

Navigate to:

**ALMA Configuration → Resources → General → Call Number Mapping**

---

## Understanding the Mapping Rules

Each row in the table represents a rule for copying a call number from the bibliographic record into the **852 field** of the holdings record.

### How ALMA Processes Rules

ALMA checks rules **in order**:
1. If a rule can be applied, ALMA executes that mapping rule and **stops**.
2. If a rule does not apply, ALMA moves on to the **next rule**.

### The 852 First Indicator: Shelving Schemes

The number in the **852 first indicator** column represents the shelving scheme associated with the holding:

| Indicator | Shelving Scheme |
|-----------|----------------|
| 0 | Library of Congress Classification |
| 1 | Dewey Decimal Classification |
| 2 | National Library of Medicine Classification |

### Reading a Rule Row — Example

Using the first row as an example:

1. **Check 852 first indicator** — If it is `0`, ALMA continues evaluating this rule. If not, ALMA looks for the first rule in the list with that indicator.
2. **Check 852 subfield 2** — If it is empty, proceed.
3. **Check bib record field 090** — If the 090 field exists (with any indicators), continue.
4. **Check for subfields A and B** — If both exist, ALMA copies:
   - 090 subfield A → 852 subfield H
   - 090 subfield B → 852 subfield I

> **Note on indicator notation:** Question marks (`?`) indicate that any value is acceptable. For example, `050?4` means the first indicator of the 050 field can be any value, but the second indicator **must be 4** for the rule to apply.

### Important: All Criteria Must Be Met

A rule is only executed if **all criteria are met exactly**. For example, if a bib record's 090 field has only subfield A (no subfield B), the rule for copying both A and B will be skipped. In that case, you would need to add a separate rule.

---

## Customizing the Mapping Table

### Adding a New Rule

To add a rule (for example, to copy subfield A alone):

1. Scroll down to the rule entry area.
2. For **Bib Subfields to Copy**, enter: `A`
3. For **852 Subfield Destinations**, enter: `H`
4. Click **Add**.

### Reordering Rules

Use the **up/down arrows** to change a rule's position in the list. Rules are evaluated in order, so placement matters.

> In the example above, the new single-subfield rule should come *after* the rule that copies both subfields A and B, so the more specific rule is checked first.

### Disabling vs. Deleting Rules

While it is possible to delete a rule, it is better practice to **disable it** using the toggle switch. This preserves the rule in case you need it later.

### Saving Your Changes

Always click **Save** after making any modifications to the table.

---

## Practical Example: Creating a Holdings Template for a Dewey Decimal Library

This example walks through a scenario where an institution uses Library of Congress classification broadly, but uses **Dewey Decimal** for its education library.

### The Relevant Mapping Rule

This workflow relies on the following rule:

> When the **852 first indicator is 1** (Dewey Decimal) and **852 subfield 2 is blank**, ALMA will copy **082 subfields A and B** (if they exist) into **852 subfields H and I** of the holdings record.

### Step 1: Open the Metadata Editor

1. Exit ALMA Configuration.
2. Open the **Metadata Editor**.
3. Select **Templates → Holdings**.

### Step 2: Duplicate an Existing Template

The easiest way to create a new template is to duplicate an existing one:

1. Right-click on an existing template (e.g., *Books*) and select **Duplicate**.
2. Enter a new **name** and, optionally, a **description**.
3. Choose the template's visibility:
   - **Private** — available only to you
   - **Shared** — available to all users at your institution
4. Optionally, set this as your **default holdings template** by checking the box.

### Step 3: Edit the Holdings Template

1. Select the new template from the list on the left.
2. Open the **852 field** in the form editor.
3. Set the **location** to your education library.
4. Set the **first indicator to `1`** (Dewey Decimal).
5. Add any additional details as needed.
6. Click **Save**.

### Step 4: Apply the Template to a Bib Record

1. Open a bibliographic record.
2. Navigate back to **Templates → Holdings** and click the template name to open it.
3. The holdings record will now show the title from the bib record and the location from the template.

### Step 5: Copy the Call Number

1. Select **Record Actions → Update from Bibliographic**.
2. The call number will be automatically added, pulled from the **082 field**:
   - Subfield A → 852 subfield H
   - Subfield B → 852 subfield I

---

## When Is the Call Number Mapping Table Used?

The call number mapping table is triggered in the following situations:

- Using the **Update from Bibliographic** tool in the Metadata Editor
- **Saving a new holdings record** in the Metadata Editor
- Running an **import job**
- Running the **Change Holding Information** job

---

## Summary

By customizing the call number mapping table, you can control exactly how call numbers are transferred from bibliographic records to holdings records across a variety of workflows. Combined with holdings templates, this gives you a powerful and flexible way to manage classification schemes — including supporting multiple schemes (such as LC and Dewey) within the same institution.
