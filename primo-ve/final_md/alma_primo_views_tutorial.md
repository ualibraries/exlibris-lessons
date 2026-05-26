# Primo VE Views: Configuration and Management Tutorial

## Overview

Views in Primo VE define everything that patrons see when they access your institution's catalog — search interfaces, results displays, menus, and available services. You can have an unlimited number of views per institution, allowing for configurations such as:

- A test view, demo view, and production view
- Separate views for different library branches

All Primo VE configuration is done through ALMA.

---

## Accessing Views

Navigate to:

**ALMA → Discovery → Display Configuration → Configure Views**

This page lists all views currently configured at your institution. The **default view** is indicated by a blue radio button — this is the view used when staff click the Display in Discovery link from a record.

---

## Creating a New View

You have two options:
- **Duplicate** an existing view (recommended for test copies of your current configuration) — use the Row Action tool and select **Duplicate**
- **Add View** — create a new view from scratch

### View Configuration Fields

On the View Configuration page, required fields are marked with a red asterisk:

**Define View section:**
- **Code** — forms part of the view's URL. Spaces and special characters are not supported.
- **Name** and optional **Description**

**General Attributes section:**
- **Guest user idle timeout** — how long before an unauthenticated user is logged out
- **Signed-in user idle timeout**
- **Default language** (e.g., English)

Click **Save and Continue** to save and keep editing, or **Save** to return to the views list.

---

## Row Action Options for Views

From the Row Action tool next to any view, you can:
- **Go to View** — open the view in a new browser tab
- **Edit** — open the view for configuration
- **Duplicate** — copy the view
- **Delete** — remove the view

---

## Editing a View

Click **Edit** to open the view configuration. The following tabs are available:

### General Tab
Displays the basic view information entered at creation. All fields are editable **except the Code**, which is tied to the view's URL.

### Links Tab
Lists the main menu links displayed in the persistent search bar.
- Toggle the **Active** column to show or hide individual links
- The **Label** column shows how each link appears to patrons
- Click **Add Link** to create a new link, or use the Row Action tool to **Edit** an existing one

### Search Profile Slots Tab
Controls the search scope options visible to users when they begin typing a query. Slots can contain one or more search profiles.

- Toggle the **Active** column to activate or deactivate a slot
- Use the **arrows** to change the display order

**Default slots include:**
- Local catalog only
- Local catalog + Central Index
- Central Index only

To create a custom slot:
1. Click **Add a Slot**
2. Enter a **Code**, **Name**, and optional description
3. Toggle which **search profiles** to include
4. Click **Save**

> For detailed search configuration, see the *Search Configuration* tutorial.

### Advanced Search Configuration Tab
Customize the options available in the advanced search interface.

### Brief Results Tab
Control facet availability, display order, and other brief results configuration elements.

> For details on these tabs, see the *Search Configuration* tutorial.

### Brief Record Display Tab
Customize the fields and actions shown for each record in the Brief Results popover.

- **Display Fields** — always four lines; change order and content using the Row Action tool → **Edit**. Delimiters determine what is shown on each line.
- **Record Actions** — the actions available to patrons when they open a record. Select up to **three up-front actions** as primary actions. Use toggles to activate or deactivate.

### Full Record Services Tab
Controls the order in which elements are displayed to patrons on the full record page.
- Use **arrows** to reorder elements
- Use the Row Action tool → **Configure** to adjust how individual areas display

---

## Summary

Views are the primary interface layer between your institution's data and your patrons. By configuring multiple views, customizing search slots, links, brief and full record displays, and service order, you can tailor the discovery experience for different user groups or library branches — all from within ALMA configuration.
