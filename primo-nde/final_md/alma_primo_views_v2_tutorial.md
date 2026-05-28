# Primo VE Views: Creating and Editing Tutorial

## Overview

Views in Primo VE define everything patrons see when they access your catalog — searches, results, and access to materials. You can have an unlimited number of views per institution, such as:

- A test view, demo view, and production view
- A separate view for each library branch

All Primo VE configuration is done through ALMA.

---

## Accessing Views

Navigate to:

**ALMA → Discovery → Display Configuration → Configure Views**

The **default view** is indicated by a blue radio button. This is the view used when staff click the Display in Discovery link from a record in ALMA.

---

## Creating a New View

Two options are available:
- **Duplicate** an existing view — ideal for creating a test copy of your current configuration (Row Action tool → **Duplicate**)
- **Add View** — create a new view from scratch

### Required Fields (marked with red asterisk)

**Define View section:**
- **Code** — forms part of the view's URL. Spaces and special characters are not supported.
- **Name** and optional **Description**

**General Attributes section:**
- **Guest user idle timeout**
- **Signed-in user idle timeout**
- **Default language**

Click **Save and Continue** to save and keep editing, or **Save** to return to the views list.

---

## Row Action Options

From the Row Action tool next to any view:
- **Go to View** — opens the view in a new browser tab
- **Edit** — opens the view for configuration
- **Duplicate** — copies the view
- **Delete** — removes the view

---

## Editing a View: Tab-by-Tab Guide

Click **Edit** to open a view. Any section not yet changed from default settings will display a **Customize** button at the top — click it to enable editing for that section.

### General Tab
Displays the basic view information. All fields are editable **except the Code**, which is tied to the view's URL.

### Links Tab
Lists the main menu links shown in the persistent search bar at the top of the view.

- Toggle the **Active** column to show or hide individual links
- Use the **arrows** to adjust display order
- The **Label** column shows how each link appears to patrons
- Click **Add Link** to create a new link
- Use the Row Action tool → **Edit** to modify an existing link

### Search Profile Slots Tab
Choose the slots available to users for narrowing searches. Slots appear in the drop-down next to the search box.

> For full details on configuring search slots, profiles, and scopes, see the *Search Configuration* tutorial.

### Advanced Search Configuration Tab
Customize the options available in advanced search.

### Brief Results Tab
Control **Quick Filters**, **Facet Availability**, **Sort**, and other search results page configuration elements.

> For full details on these tabs, see the *Search Configuration* tutorial.

### Brief Record Display Tab
Customizes the information and actions shown for each record on the Brief Results page.

**Display Fields section:**
- Always four lines; drag and drop to reorder
- Click the Row Action tool → **Edit** to change the content of a line
- Change the **delimiter** to use a different symbol between elements
- Use the **checkboxes** to display a summary and/or a snippet with each brief record

**Record Actions section:**
- Actions are grouped by type
- Choose which **action types** to display and in what order
- Click the Row Action menu to configure the individual actions within each group

### Full Record Services Tab
Lists all possible sections in the order they appear when a patron views a full record. Only relevant sections display for each title.

- Use the **checkboxes** to set a section to display **expanded by default**
- Some sections have additional configuration options via the Row Action menu

### Manage Customization Package Tab
Used to style the view's colors and branding.

> For details, see the *User Interface Customization* tutorial.

---

## Summary

Views are the patron-facing layer of Primo VE. By creating dedicated views for different use cases (testing, production, branch libraries) and carefully configuring each tab, you can give every audience the right search and display experience — all managed from within ALMA.
