# Primo VE Search Configuration: A Tutorial

## Overview

When patrons search in Primo VE, they interact with a layered system of **scopes**, **search profiles**, and **slots**. Once results appear, they can further refine using **resource type filters**, **quick filters**, and the **All Filters** side panel. As an administrator, you configure all of these elements.

---

## Key Concepts

| Component | Description |
|-----------|-------------|
| **Scope** | A group of records meeting specific conditions (e.g., a specific library, resource type, or available electronic inventory) |
| **Search Profile** | A container for one or more scopes; must contain at least one scope |
| **Slot** | A grouping of search profiles presented to users as a selectable option next to the search box |

**Example:** A patron selects the *Alma University and Central Discovery Index* slot — this contains a search profile that combines the Alma University scope and the Central Discovery Index scope. The slot menu appears to the left of the search terms in the persistent search bar.

---

## Accessing Search Profiles

Navigate to:

**ALMA → Discovery → Search Configuration → Search Profiles**

Three tabs are available:

- **Search Profiles** — all profiles configured at your institution. Default profiles include: All Catalog Records, Central Index Records, All Records + Central Discovery Index, and Course Reserves.
- **Custom Local Data Scopes** — create scopes limiting searches to specific local metadata (resource type, availability, etc.) without needing a dedicated library. Useful for special collections.
- **Other Indexes** — define third-party search indexes that can then be added to a profile.

> **Recommendation:** Do not edit existing out-of-the-box profiles. Create new profiles for your customizations.

---

## Creating a New Search Profile

1. Click **Add a Search Profile**.
2. Enter a **Code** and **Display Name** (required).
3. Use the **globe icon** to assign translated display names.
4. Click **Add Scope**.
5. In the **Select Scope Type** drop-down, choose from available campuses, libraries, or custom scope types.
   - Custom scopes you created appear under **Custom, Local Data**.
   - For a library scope, select **My Libraries**, then choose the specific library from the second drop-down.
6. Click **Add** to continue adding scopes, or **Add and Close** when finished.
7. Click **Save**.

---

## Configuring Search Slots (Basic Search)

Slots are configured within a view. Navigate to:

**ALMA → Discovery → Display Configuration → Configure Views → [Row Action: Edit]**

Go to the **Search Profile Slots** tab. This lists all slots that appear in the drop-down next to the search box.

- Toggle **Active** to show or hide individual slots
- Use the **arrows** to change display order

### Creating a New Slot

1. Click **Add a Slot**.
2. Enter a **Code**, **Name**, and optional description.
3. In **Select Search Profiles for Slots**, toggle the search profile(s) to activate.
4. Click **Save**.

---

## Configuring Advanced Search

From the same view edit page, go to the **Advanced Search Configuration** tab. Each part of advanced search is controlled by a separate list within this tab:

| Section | Controls |
|---------|----------|
| **List of Indexes** | The search index options (first drop-down in each query row) |
| **List of Resource Types** | The resource type drop-down |
| **Language** | The language filter drop-down |
| **Search Operators** | The operator options (AND/OR/NOT) |

Within each list, you can:
- Toggle individual fields **on or off**
- **Reorder** fields using the arrows

> Changes in this tab are **saved automatically**.

### Search Profile Slot Column

Some advanced search options (such as Course Instructor and Course ID) only appear when a specific slot is selected at the top of the search form. This behavior is configured in the **Search Profile Slots** column within each list.

---

## Configuring Facets, Quick Filters, and Sort (Brief Results Tab)

From the view editor, go to the **Brief Results** tab.

### Quick Filters
Commonly used filters displayed above the brief results for immediate access. Each quick filter:
- Only displays if toggled **Active**
- Can be **reordered** by drag and drop

### All Filters Side Panel (Facets)
- Toggle individual facets **on or off**
- Use **arrows** to change order
- **Values to Display** — how many values appear before the facet must be expanded
- **Sort Type** — how items within a facet are sorted (use drop-down to change)

### Resource Type Filters
Scroll down in the Brief Results tab to see resource type filters. These can be toggled active/inactive, edited, or reordered.

---

## Summary

ALMA's search configuration gives you granular control over what content patrons search, how they narrow results, and what filter options they see. By building scopes, organizing them into profiles, grouping profiles into slots, and tuning quick filters and facets, you create a targeted and intuitive discovery experience.
