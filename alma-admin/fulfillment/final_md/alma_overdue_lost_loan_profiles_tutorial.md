# ALMA Overdue and Lost Loan Profiles: A Configuration Tutorial

## Overview

Overdue and Lost Loan Profiles monitor overdue loans and — when configured — convert them to lost loans. These profiles can:

- Send notification letters to patrons at progressive overdue intervals
- Create overdue loan fines
- Apply user blocks
- Change a loan's status to lost

ALMA runs the **Loans, Overdue and Lost Item** job daily to process overdue and lost loans according to your configured profiles.

---

## Accessing Overdue and Lost Loan Profiles

Navigate to:

**ALMA Configuration → Fulfillment → Physical Fulfillment → Overdue and Lost Loan Profile**

This page lists all current profiles. From here you can:
- **Enable or disable** a profile using the toggle in the Enable column
- Mark whether a profile should **create an overdue loan fine**
- Use the **Row Action** tool to **Edit**, **Duplicate**, **Delete**, or **Run Now** (generates notifications for that profile on demand)

---

## Editing a Profile

Click the **Row Action** tool and select **Edit** to open the profile record.

Key fields include:

- **Profile Type** — determines the profile's behavior:
  - **Change to Lost** — items meeting the criteria are marked lost; the *Send Notification*, *Create Overdue Loan Fine*, and *Create Block* checkboxes are hidden, and the Letter Send Format field becomes required
  - **Overdue Notification Type 1–5** — sends notifications without marking items lost
- **Notification Letters** — configure up to **five progressive letters** sent to the patron based on how many days overdue the loan is

  > For information on configuring letters, see the Knowledge Center.

- **Fine Amount** — if the profile is set to create a fine, the amount is determined by the profile type and the applicable Terms of Use policy.

Click **Save** when done.

---

## Creating a New Profile

1. Click **Add Overdue and Lost Loan Profile**.
2. Enter a **Profile Name** and optional description.
3. Check **Active** if you want the profile to be enabled immediately.
4. Select the **Profile Type** (e.g., *Overdue Notification Type 2*).
5. Fill in the remaining criteria as needed.

   > **Note:** If any fields are left blank, the profile will apply to all items matching that criterion.

6. Click **Save**.

After saving, you may be prompted to run a **Status Update** on the profile. This marks any existing loans that would be impacted by your new or changed profile, preventing them from being retroactively handled the next time the associated job runs.

---

## Enabling the Status Update Feature

The **Status Update** feature allows you to run the overdue and lost loan job without creating blocks, fines, changing loans to lost, or generating notifications. It simply marks loans so they are not handled again by matching profiles.

### Activating Status Update

Navigate to:

**ALMA Configuration → Fulfillment → General → Other Settings**

1. Scroll to the **Switch to Overdue and Lost Loan New Job** parameter.
2. If it is not set to **True**, click the **Row Action** tool, select **Edit**, and change the value to *True*.
3. Click **Save**.

Once enabled, **Status Update** will appear as an option in the Row Action menu of the Overdue and Lost Loan Profile list.

---

## Summary

Overdue and Lost Loan Profiles are a powerful tool for automating patron communication and account management. By configuring progressive notifications, fine creation, and block triggers — and using the Status Update feature when making changes — you can ensure that your overdue workflows are both effective and fair to patrons with existing loans.
