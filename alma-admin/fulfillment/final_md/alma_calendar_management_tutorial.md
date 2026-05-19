# ALMA Calendar Management: A Tutorial

## Overview

Calendars in ALMA manage the open and closed dates and hours for your institution and its libraries. Accurate calendars are important because fulfillment policies — such as due date calculations — rely on them.

In this tutorial, you will learn how to:
- Update institution-level and library-level calendar records
- Add closure dates and exceptions
- Bulk update due dates after a calendar change
- Verify that the Due Date Correction job is scheduled correctly

---

## Understanding Calendar Levels

ALMA has two calendar levels:

| Level | Purpose |
|-------|---------|
| **Institution** | Events and exceptions that apply to all libraries (inherited downward) |
| **Library** | Standard opening hours and library-specific exceptions; **not** inherited from institution |

> Standard Opening Hours must be defined at the **library level** for each library. Fulfillment policies rely on these settings.

---

## Accessing Institution-Level Calendars

Navigate to:

**ALMA Configuration → General → Libraries → Add a Library or Edit Library Information**

1. Select the **institution level** from the Configuring menu.
2. Click the **Calendar Management** tab to see all current institution-level calendar records, including hours, exceptions, and events.
3. Click **Full Calendar** to preview the calendar in day, week, or month view. Days that are blank are closed days.
4. Click **Back** when done.

---

## Types of Calendar Records

When adding a record at either level, you will choose from three types:

| Type | Purpose |
|------|---------|
| **Event** | Special dates (e.g., end of semester, exhibitions). Does not indicate open or closed status. |
| **Exception** | Open or closed dates outside the standard schedule (e.g., holidays, one-time closures) |
| **Standard Opening Hours** | Regular recurring open hours |

---

## Adding an Institution-Level Closure Date

1. From the **Institution Calendar Management** tab, click **Add Record**.
2. Select **Exception** as the record type.
3. Fill in the date information (e.g., *Independence Day*).
4. Click **Add** to continue adding records, or **Add and Close** when finished.
5. Click **Apply Changes** to run the Calendar Changes job and update the system.
6. Click **Save**.

> **Note:** Closed dates that fall on a different day each year (such as some holidays) must be **updated annually**.

You can also **import bulk changes** by clicking **Import**. For details, see the *Update Library Opening Hours via Excel Import* session on the Ex Libris YouTube channel.

---

## Adding a Library-Level Calendar Record

Library-specific exceptions are added at the library level.

1. Select your **library** from the Configuring menu.
2. Navigate to: **Fulfillment → Library Management → Standard Opening Hours**
3. Records inherited from the institution level will display a **green checkmark** in the Inherited column and will not have a Row Action menu.
4. Click **Add Record** to create a library-specific record.
5. Select **Exception** for a one-time occurrence (e.g., a staff training day).
6. Enter a **description** and set the **Valid From** and **Valid To** dates.
   - If the closure is only partial (e.g., a half day), set specific hours.
   - For a full-day closure, leave hours at the default.
7. Click **Add and Close**.
8. Click **Apply Changes** to run the associated job.
9. Click **Save**.

---

## Bulk Updating Due Dates After a Calendar Change

If a calendar change affects existing loans — such as an unexpected closure — you can update due dates in bulk and potentially waive any fines created by the change.

Navigate to:

**ALMA → Fulfillment → Advanced Tools → Loans → Bulk Change Due Dates**

1. Enter:
   - The **library** the changes apply to
   - The **material types** affected
   - The **range of current due dates** to update
   - The **new due date**
2. Click **Change Bulk Due Date**.
3. Click **Confirm**.

The job is added to the queue and will appear in the table below once complete. Previous bulk due date changes are also visible here.

---

## Verifying the Due Date Correction Job

To keep loans aligned with calendar changes on an ongoing basis, verify that the **Loans, Due Date Correction After Calendar Change** job is scheduled to run daily.

Navigate to:

**ALMA → Admin → Manage Jobs and Sets → Monitor Jobs → Scheduled tab**

Use the dropdown to filter by **Fulfillment** jobs and confirm that this job is scheduled to run every day. You can also run it manually at any time.

---

## Summary

Maintaining accurate calendars in ALMA ensures that due dates, fine calculations, and fulfillment policies all reflect your library's actual hours. By managing exceptions at the correct level (institution vs. library), running the Apply Changes job after updates, and keeping the Due Date Correction job on a daily schedule, you can prevent calendar-related errors from affecting your patrons.
