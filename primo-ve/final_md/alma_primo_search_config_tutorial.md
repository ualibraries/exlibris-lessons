# Primo VE Search Configuration: A Tutorial

## Overview

When a patron searches in Primo VE, they interact with a layered system of **scopes**, **search profiles**, and **slots** that determine what content is searched and how results are filtered and sorted. As an administrator, you configure each of these layers, as well as the options available in basic and advanced search.

---

## Key Concepts

| Component | Description |
|-----------|-------------|
| **Scope** | A group of records meeting specific conditions (e.g., a specific library, resource type, or electronic inventory) |
| **Search Profile** | A container for one or more scopes; used to search in Primo VE. Must contain at least one scope. |
| **Slot** | A grouping of one or more search profiles; displayed to users as a selectable search option when they begin typing |

**Example:** A patron selects the *Alma University and Central Index* slot, which contains a search profile combining the Alma University scope and the Central Discovery Index scope.

---

## Accessing Search Profiles

Navigate to:

**ALMA → Discovery → Search Configuration → Search Profiles**

This page has three tabs:

- **Search Profiles** — all profiles configured at your institution. Out-of-the-box profiles include: All Catalog Records, Central Index Records, All Records + Central Discovery Index, and Course Reserves.
- **Custom Local Data Scopes** — create scopes that limit searches to specific local metadata (e.g., resource type, availability) without needing a dedicated library. Useful for special collections.
- **Other Indexes** — define third-party search indexes, which can then be added to a search profile.

> **Note:** It is recommended that you do not edit existing out-of-the-box profiles. Create new profiles for your customizations instead.

---

## Creating a New Search Profile

1. Click **Add a Search Profile**.
2. Enter a **Code** and **Display Name** (required).
3. Use the **globe icon** to assign translated display names if needed.
4. Click **Add Scope**.
5. In the **Select Scope Type** drop-down, choose from the available campuses, libraries, or custom scope types.
   - To add a custom local data scope you created, look under **Custom, Local Data**.
   - To add a library scope, select **My Libraries**, then choose the specific library from the second drop-down.
6. Click **Add** to continue adding more scopes, or **Add & Close** when finished.
7. Click **Save**.

---

## Configuring Basic Search: Search Profile Slots

Slots appear in the search bar as selectable options when patrons begin typing. They are configured within a view.

Navigate to:

**ALMA → Discovery → Display Configuration → Configure Views → [Row Action: Edit]**

Go to the **Search Profile Slots** tab.

- Use the **toggle** to activate or deactivate individual slots
- Use the **arrows** to change the display order

### Creating a New Slot

1. Click **Add a Slot**.
2. Enter a **Code**, **Name**, and optional description.
3. In the **Select Search Profiles for Slots** section, toggle to activate the search profile(s) to include.
4. Click **Save**.

---

## Configuring Advanced Search

From the same view edit page, click the **Advanced Search Configuration** tab.

This lists all sections of the advanced search menu and their contents. For each section you can:
- **Toggle** individual fields on and off
- **Reorder** fields using the arrows
- Use the Row Action tool to **Edit** or **Delete** a field

> If a section appears non-editable, click **Customize** in the top right of that section.

**Enable for Basic Search** checkbox — adds pre-filters beneath the persistent search bar for basic search users.

> Changes in this tab are saved automatically.

---

## Configuring Facets and Sort

Facet and sort options are configured under the **Brief Results** tab in the view editor.

For each facet you can:
- **Toggle** it on or off
- **Reorder** it using the arrows
- Set **Values to Display** — how many values appear before the facet must be expanded
- Set **Sort Type** — how items within the facet are sorted (use the drop-down to change)

---

## Summary

ALMA's search configuration system gives you granular control over what content patrons can search, how search options are presented, and how results can be filtered. By carefully building scopes, organizing them into profiles, grouping profiles into slots, and tuning advanced search and facets, you can create a highly tailored discovery experience for your users.
