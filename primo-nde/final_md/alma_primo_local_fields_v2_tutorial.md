# Primo VE Local Fields and Local Resource Types: A Configuration Tutorial

## Overview

**Local fields** allow you to map additional metadata from bibliographic records for display, search, and faceting in Primo VE beyond what is available by default. **Local resource types** let you create discoverable content categories — such as exam papers, book chapters, or case law — that are not covered by standard rules.

In this tutorial, you will learn how to:
- Create local fields using two methods
- Customize default display fields
- Test normalization rules before re-indexing
- Create local resource types

---

## What Local Fields Enable

Local fields let you use information from bibliographic records to:
- **Extend search queries** with additional indexed fields
- **Filter search results** using custom facets
- **Display additional information** in brief and full record views

---

## Two Methods for Creating Local Fields

### Method 1: Bibliographic Field Method

Directly maps fields from supported MARC record types or Dublin Core.

**Use this method when:**
- The field is in a supported format
- The mapping is not conditional
- You want to map the field as-is

**Limits:** Up to 100 local fields for MARC records, 50 for Dublin Core records.

### Method 2: Normalization Rules Method

Uses custom normalization rules to map MARC or Dublin Core fields to local display, search, and facet fields.

**Limits:** Up to 10 local facet/search fields.

> **Consortium note:** If one member institution uses this method for a local field, other members should not use the same field unless they use identical normalization rules or switch to the Bibliographic Field Method — otherwise data may be overwritten.

> **Re-indexing note:** Changes to local **search and facet** fields via normalization rules require contacting support to re-index records. Changes to **display** fields do not require re-indexing.

---

## Accessing Local Fields

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Search Display → Local Fields**

Fields named *Local Field* use the Bibliographic Field Method. Fields without that label are display fields defined by normalization rules.

---

## Creating a New Local Field

1. Click **Add Field → Add Local Field**.
2. Select a **field** from the drop-down (only available local fields are shown).
3. Enter a **display label**.
4. The **Local Field Details** section appears:
   - Check **Search** to add a local search index
   - Check **Facet** to add a local facet

### Bibliographic Field Method (MARC 21)
- Click **Add MARC 21 Fields** and select the desired field(s) from the drop-down.
- Note: If you cannot find the field you need and do not see the option to add normalization rules for search and facet, you may need to define the local field on the **Local Fields Using Search and Facet Normalization Rules** page. See the Knowledge Center for details.

### Normalization Rules Method

Choose one of two rule types:

**Normalization Rules for Display:**
- Maps any MARC 21 field to a local display field
- Overrides any mappings in the MARC 21 Fields section
- Edit: Row Action tool → **Edit**, replace `XXX` with the field number and subfield
- **No re-indexing required**; click **Apply Rules** to put changes into effect immediately

**Normalization Rules for Search and Facet:**
- Maps any MARC 21 field to a local search and facet field
- If using this method, you **cannot** use the Bibliographic Field Method for display — create separate normalization rules for display and for search/facet
- **Re-indexing required** — contact support after making changes

Click **Save** when done.

---

## Testing a Normalization Rule

Before committing to re-indexing, test a search/facet normalization rule against a real record:

1. Open the local field → Row Action tool → **Edit**.
2. Open the Row Action tool for the MARC 21 normalization rule for search and facet → **Test**.
3. In the pop-up, perform a **repository search** to find a catalog item.
4. The normalized result displays below the search — verify it returns the expected value.
5. Click **Close** when done.

---

## Customizing Default Display Fields

To modify what appears for a record using an existing out-of-the-box display field:

1. On the Manage Display and Local Fields page, click **Add Field → Add Display Field**.
2. Select an out-of-the-box field from the **Field to Edit** drop-down — its normalization rules will populate.
3. Click the Row Action tool → **Edit** and make your changes.
4. Click **Save**, then **Back**.
5. Click **Apply Rules** to put changes into effect immediately (display changes do not require re-indexing).

---

## Creating Local Resource Types

Local resource types surface content categories not covered by standard metadata rules.

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Local Resource Types**

### Adding a New Local Resource Type

1. Click **Add Local Resource Type**.
2. Fill in the **General** section (required):
   - **Code**
   - **Display Singular Label**
   - **Display Plural Label**
3. In **Mapping from MARC Records**, click **Add Condition**:
   - Specify the **MARC field and subfield** containing the resource type value
   - In **Value in MARC**, enter the matching value(s)
   - Use a **semicolon** to separate multiple values (e.g., `EXA;EX;Examination Paper`)
   - Optionally use a **regular expression** for conditional matching

   **Regex example:** To match a MARC field where the character at position 33 is A, O, or C:
   ```
   .{32}[AOC]
   ```
   This matches any 32 characters followed by A, O, or C in the 33rd position.

4. Add **conditional logic** between multiple conditions if needed.
5. Click **Save**.

If the resource type was not set to Active during creation, use the **toggle** on the list page to activate it.

---

## Summary

Local fields and local resource types extend Primo VE's discovery capabilities beyond standard configurations. By choosing the right mapping method, testing normalization rules before re-indexing, and creating local resource types for special collections, you can meaningfully enrich the patron search experience with institution-specific metadata.
