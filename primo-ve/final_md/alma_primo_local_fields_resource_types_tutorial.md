# Primo VE Local Fields and Local Resource Types: A Configuration Tutorial

## Overview

**Local fields** allow you to extend what can be searched, faceted, and displayed in Primo VE using metadata from your bibliographic records that is not mapped by default. **Local resource types** let you surface locally defined content categories — such as exam papers, book chapters, or case law — that are not covered by out-of-the-box resource type rules.

In this tutorial, you will learn how to:
- Create local fields using two different methods
- Customize default display fields
- Test normalization rules before re-indexing
- Create local resource types

---

## Understanding Local Fields

Local fields let you use bibliographic record data to:
- **Extend search queries** with additional indexed fields
- **Filter search results** using custom facets
- **Display additional information** in brief and full record views

---

## Two Methods for Creating Local Fields

### Method 1: Bibliographic Field Method

Maps fields directly from supported MARC record types or Dublin Core.

**Use this method when:**
- The field is in a supported format
- The mapping is not conditional (not based on subfield content or another field)
- You want to map the field as-is

**Limits:** Up to 100 local fields for MARC records, 50 for Dublin Core records.

### Method 2: Normalization Rules Method

Uses custom normalization rules to map MARC or Dublin Core fields to local display, search, and facet fields.

**Use this method when:**
- You need conditional field mapping
- You need greater flexibility in transformation

**Limits:** Up to 10 local facet/search fields.

> **Consortium note:** If a member institution uses this method, the same local field should not be used by other members unless they use the same normalization rules or the Bibliographic Field Mapping Method, as data may be overwritten.

> **Re-indexing note:** Changes to local search and facet fields via normalization rules require contacting support to re-index records. Display field changes do **not** require re-indexing.

---

## Accessing Local Fields

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Search Display → Local Fields**

This page lists all mapped fields. Fields named *Local Field* use the Bibliographic Field Method. Fields without that prefix are display fields defined by normalization rules.

---

## Creating a New Local Field

1. Click **Add Field → Add Local Field**.
2. Select the **field to edit** from the drop-down (only available local fields are shown).
3. Enter a **display label**.
4. When you select the field, the **Local Field Details** section appears:
   - Check **Search** to add a local search index
   - Check **Facet** to add a local facet

### Using the Bibliographic Field Method (MARC 21)
- Click **Add MARC 21 Fields** and select the desired field(s) from the drop-down.

### Using the Normalization Rules Method

Choose whether to configure:

**Normalization Rules for Display:**
- Maps any MARC 21 field to a local display field
- Overrides any mappings defined in the MARC 21 Fields section
- To edit: click the Row Action tool → **Edit**, then replace `XXX` with the field number and subfield
- **No re-indexing required**

**Normalization Rules for Search and Facet:**
- Maps any MARC 21 field to a local search/facet field
- If using this for search/facet, you **cannot** use the Bibliographic Field Method for display — you must create separate normalization rules for display and for search/facet
- **Re-indexing required** — contact support after enabling

Click **Save** when finished. For display rules only, click **Apply Rules** to put changes into effect immediately.

---

## Testing a Normalization Rule

Before committing to re-indexing, you can test a search/facet normalization rule against a real record:

1. Open the local field and click the Row Action tool for the normalization rule → **Test**.
2. In the pop-up, perform a **repository search** to find an item.
3. The normalized result will display below — verify it returns the expected value.
4. Click **Close** when done.

---

## Customizing Default Display Fields

To change what is displayed for a record using existing out-of-the-box display fields:

1. On the Manage Display and Local Fields page, click **Add Field → Add Display Field**.
2. Select an out-of-the-box display field from the **Field to Edit** drop-down.
3. The normalization rules for that field will populate.
4. Click the Row Action tool → **Edit** and make your changes.
5. Click **Save** and then **Back**.
6. Click **Apply Rules** (for display-only changes) — these take effect without re-indexing.

---

## Creating Local Resource Types

Local resource types allow patrons to discover content categories not covered by standard metadata rules (e.g., *Exam Papers*, *Book Chapters*, *Case Law*).

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Local Resource Types**

### Adding a New Local Resource Type

1. Click **Add Local Resource Type**.
2. Fill in the **General** section (required fields):
   - **Code**
   - **Display Singular Label**
   - **Display Plural Label**

3. In the **Mapping from MARC Records** section, click **Add Condition**:
   - Specify the **MARC field and subfield** that contains the resource type value
   - In **Value in MARC**, enter the specific value(s) to match
   - Use a **semicolon** to separate multiple possible values (e.g., `EXA;EX;Examination Paper`)
   - Optionally, use a **regular expression** to extract values conditionally

4. If you add more than one condition, you can apply **conditional logic** between conditions.

5. Click **Save**.

If you did not check the **Active** box during creation, use the **toggle** on the list page to activate the resource type when ready.

---

## Summary

Local fields and local resource types give you the flexibility to surface institution-specific metadata in Primo VE that standard configurations cannot. By choosing the right mapping method, testing rules before re-indexing, and activating local resource types for special collections, you can significantly enrich the discovery experience for your patrons.
