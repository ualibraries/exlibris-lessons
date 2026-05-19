# ALMA Fulfillment Configuration Utility: A Tutorial

## Overview

The **Fulfillment Configuration Utility** allows you to look up the fulfillment attributes that would apply to a specific patron borrowing a specific item. It shows you — in real time — what loan terms, due dates, fines, request options, and overdue profiles would be in effect, without actually creating a transaction.

This is especially useful for:
- Answering patron questions about due dates or fines
- Troubleshooting why a particular loan policy is being applied
- Verifying that fulfillment configuration changes are working as expected

---

## Accessing the Fulfillment Configuration Utility

Navigate to:

**ALMA → Fulfillment → Advanced Tools → Loans → Fulfillment Configuration Utility**

---

## Looking Up a Patron and Item

You can identify the patron in two ways:
- **Enter their name or primary identifier** directly
- **Select from a list**

Repeat the same process for the **item barcode**.

Click **OK** once both fields are filled in.

---

## Reading the Utility Results

The utility displays:

- **Fulfillment Unit Name and Rule** — the fulfillment unit and rule being applied to this loan
- **Terms of Use** — the Terms of Use in effect for this item and patron combination
- **Due Date** — the date the item would be due if checked out right now

Click on any **fulfillment attribute name** to view and edit it directly.

> For more information about Fulfillment Units, see the Fulfillment Units tutorial in the Alma Essentials Training in the Knowledge Center.

---

## Calculating an Overdue Fine

If a patron knows they will return an item late, you can calculate the anticipated fine:

1. Enter the **anticipated return date** in the provided field.
2. Click **Calculate Overdue Fine**.

ALMA will display the fine that would accrue based on the applicable Terms of Use policy.

---

## Additional Tabs

The utility includes tabs for requests, bookings, and overdue profiles:

### Request Tab
Displays the fulfillment attributes applicable to a **request** for the selected item by this patron. Click on any attribute name to view and edit it.

### Booking Tab
Displays the fulfillment attributes applicable to a **booking request** for the selected item. As with the other tabs, attributes are clickable and editable.

### Overdue and Lost Loan Profiles Tab
Displays which **overdue and lost loan profiles** would apply to a given overdue loan for this patron and item combination.

---

## Summary

The Fulfillment Configuration Utility is a quick and non-destructive way to test and verify your fulfillment setup. By entering a patron and item, you can see exactly which rules and policies ALMA would apply — and follow links directly to those configurations to make adjustments if needed.
