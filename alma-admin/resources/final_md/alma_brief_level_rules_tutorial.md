# ALMA Brief Level Rules: A Configuration Tutorial

## Overview

A **Brief Record Level** is a value assigned to bibliographic records in ALMA to indicate their level of completeness. Brief levels serve several important purposes:

- **Protect full records** — prevent a complete record from being overlaid by a briefer version during import
- **Enable targeted searching** — allow staff to search for records by brief level from advanced search
- **Support batch updates** — identify brief records so they can be updated later via a job

Brief levels are defined on a scale from **0.1** (most brief) to **10** (full record), and are assigned automatically using **brief level rules**.

In this tutorial, you will learn how to:
- Understand and use the out-of-the-box brief level rules
- Duplicate or create a new brief level rule
- Test a brief level rule against a bibliographic record
- Set a default brief level rule
- Run a job to assign brief levels to a set of records

---

## Understanding Brief Level Rules

Brief level rules use the same syntax as normalization rules. They evaluate the metadata present in a bibliographic record and assign a level accordingly.

### Example Rule Logic

| Condition | Level Assigned |
|-----------|---------------|
| No 245 field with subfield A | 0.1 |
| No 050 subfield A **and** no 082 subfield A | 0.2 |
| *(additional conditions...)* | *(intermediate levels)* |
| All conditions passed (full record) | 10 |

The rule works through conditions in order. At the end, when all other conditions have been checked, it defaults to a level of **10**, representing a full record.

---

## Viewing Out-of-the-Box Rules

ALMA ships with several pre-built brief level rules. To view them:

1. Open the **Metadata Editor**.
2. Go to **Rules → Brief Level**.
3. Under the **Shared** folder, select a rule (e.g., *Brief Based on Record Content MARC 21*) to examine its syntax.

> **Note:** Out-of-the-box brief level rules **cannot be edited or deleted**. Many libraries find these rules meet their needs without modification — review them before deciding to create your own.

---

## Creating a Brief Level Rule

### Option 1: Duplicate an Existing Rule

If you need a rule similar to an existing one:

1. Select the rule you want to copy.
2. Click **Duplicate**.
3. In the rule properties box that appears:
   - Update the **name** and **description**
   - Select either **Private** or **Shared**
4. The new copy is added to the **Shared** folder and is ready to edit.

### Option 2: Create a Brand New Rule

1. In the Metadata Editor, go to **New → Brief Level**.
2. Enter a **name** and **description**.
3. Choose **Shared** and click **Save**.
4. The rule editing pane opens, blank and ready for input.
5. Add your rule syntax.
6. Click **Save** when finished.

The new rule will appear in the **Shared** folder.

---

## Testing a Brief Level Rule

Before deploying a rule, you can test its logic against a real bibliographic record:

1. Open a **bibliographic record** in the Metadata Editor.
2. Click the **Split Editor** icon to open a side-by-side view.
3. Open the brief level rule you want to test.
4. Click **Try It**.

ALMA will apply the rule to the open bibliographic record and display a message indicating the level it would assign.

---

## Setting a Default Brief Level Rule

The default brief level rule is the one ALMA uses automatically whenever you:
- Save a record in the Metadata Editor
- Run the **Identifying Brief Level** job

To set a default rule:

1. Navigate to: **ALMA Configuration → Resources → Cataloging → Metadata Configuration**
2. Select the appropriate profile (e.g., **MARC 21 Bibliographic**).
3. Click the **Other Settings** tab.
4. In the **Brief Level Rule** parameter, open the dropdown and select the rule you want to use as the default.
5. Click **Save** and confirm.

---

## Running the Identifying Brief Level Job

To assign brief levels to a set of records in bulk:

1. Go to: **ALMA → Admin → Run a Job**
2. Search for **brief level** to locate the job.
3. Select **Identifying Brief Level** and click **Next**.
4. Select the **set of records** on which you want to run the job.
5. Click **Next**, review the summary, and click **Submit**.
6. Confirm to start the job.

### Monitoring the Job

- Click **Refresh** to check progress while the job is running.
- Go to the **History** tab to confirm the job completed successfully.

---

## Summary

Brief level rules give your institution a consistent, automated way to measure and track the completeness of bibliographic records. By leveraging the out-of-the-box rules (or customizing your own), setting a default rule, and running the identifying brief level job, you can keep your catalog quality high and ensure that full records are never overwritten by less complete versions.
