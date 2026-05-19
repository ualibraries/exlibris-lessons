# ALMA Search Index Configuration: A Customization Tutorial

## Overview

In ALMA, searches begin by choosing a **search type**, then a **search index** (the field to search), followed by the search term. Administrators can configure which search indexes appear in both simple and advanced searches — streamlining the experience for users and removing indexes that are never used.

In this tutorial, you will learn how to:
- Configure which search indexes are available for simple and advanced searches
- Disable indexes your institution does not use
- Rename local field labels to reflect your institution's terminology

---

## Understanding Search Indexes

When users perform a search in ALMA — whether from the persistent search bar (simple search) or the advanced search interface — they see a dropdown list of available search indexes. As an administrator, you control which indexes appear in each dropdown.

**Local fields** are record fields reserved for institution-specific information. They begin with numbered labels (e.g., 902), but you can rename them to reflect how they are actually used at your institution (e.g., changing *Local Field 902* to *Project Code*).

---

## Accessing the Search Indexes Table

Navigate to:

**ALMA Configuration → Resources → Search Configuration → Search Indexes**

This table lists all search indexes **alphabetically by index code**. For each index you can see:
- A **toggle switch** to enable or disable the index entirely
- A **Simple Search** column — whether the index appears in the simple search dropdown
- An **Advanced Search** column — whether the index appears in the advanced search dropdown

---

## Limiting Simple Search Indexes

Many institutions prefer to keep the simple search dropdown short, displaying only the most frequently used indexes. Less common indexes can be removed from simple search while remaining available in advanced search.

### Steps to Remove an Index from Simple Search

1. Locate the index you want to change in the table.
2. Click the **Row Action** button, then select **Customize**.
3. Change the **Simple Search** column value from `True` to `False`.
4. Leave **Advanced Search** set to `True`.
5. Repeat for any other indexes you want to adjust.
6. Click **Save**.

---

## Disabling Indexes Entirely

If your institution never uses a particular set of indexes, you can disable them so they do not appear in either simple or advanced search.

### Example: Removing Dublin Core Indexes

If your institution does not use Dublin Core records, you may want to remove all indexes beginning with `DEC`:

1. Locate the index in the table.
2. Click the **Row Action** button, then select **Customize**.
3. Switch the toggle to **Disable the Index**.
4. Click **Save**.

A disabled index will not appear in either simple or advanced search, regardless of the values in the Simple Search or Advanced Search columns.

> **Best practice:** Think carefully before disabling an index. If you do disable one, **document the decision** so your staff is aware that it can be re-enabled in the future.

---

## Finding Indexes More Easily

If you need to locate a specific index, it may be easier to:

1. Click the **Export List** icon to export the full table.
2. Open the exported file in **Excel**.
3. Use **Filters** and the **Find** tool to locate the index quickly.

To look up the index code for a particular search index label, refer to the table in the ALMA Online Help article: *Configuring What Search Indexes Are Available*.

---

## Renaming Local Field Labels

Only **local field labels** can be renamed. These are fields in each record that your institution uses for its own purposes. Renaming them makes the search interface more intuitive for your staff.

### Steps to Rename a Local Field Label

1. Navigate to: **ALMA Configuration → Resources → Search Configuration → Customize Index Labels**
2. Locate the local field you want to rename.
3. Change the **Description** to your preferred label (e.g., change *Local Field 902* to *Project Code*).
4. Click **Save**.

---

## Making a Local Field Available as a Search Index

After renaming a local field, you may also want to make it searchable:

1. Return to **ALMA Configuration → Resources → Search Configuration → Search Indexes**.
2. Locate the local field in the table.
3. **Enable** the field using the toggle switch.
4. Set it to display in **Simple Search**, **Advanced Search**, or both, as desired.

---

## Applying Your Changes

> **Important:** After making any configuration changes, you must **sign out of ALMA and sign back in** to see the updates take effect.

---

## Summary

Configuring ALMA's search indexes gives administrators fine-grained control over the search experience. By limiting simple search to the most-used indexes, disabling irrelevant ones, and giving local fields meaningful names, you can reduce clutter and make ALMA easier to use for everyone at your institution.
