# ALMA License Terms Configuration: A Tutorial

## Overview

When creating or editing licenses in ALMA, the **License Terms** tab is where the conditions of the license are defined. This tab is divided into **sections** (such as *Terms of Use*, *Restrictions*, and *Obligations*), each of which contains individual **license terms** (such as *Digital Copy* or *Remote Access*).

As an ALMA administrator, you can control:
- The **order** in which sections appear on the License Terms tab
- Which **sections** are visible
- Which **license terms** appear within each section
- The **display order** of terms within a section
- Whether a term is **visible to library patrons** in Discovery

In this tutorial, you will learn how to:
- Reorder license sections
- Enable and disable sections
- Add license terms to a section
- Control the display order and public visibility of terms

---

## Reordering License Sections

Navigate to:

**ALMA Configuration → Acquisitions → Licenses → Sections Order**

This page lists all available license sections.

### Enabling and Disabling Sections

- Use the toggle next to any section to **disable** it (it will not appear on the License Terms tab at all) or **enable** it to make it visible.

### Changing Section Order

To rearrange sections (e.g., to place *Obligations* above *Perpetual Rights*):

1. For each row in the table, use the drop-down to select which section should appear in that position.
2. Rearrange rows until the order reflects your preference.
3. Click **Save**.

The new section order will be reflected the next time a license is opened.

---

## Managing License Terms

Navigate to:

**ALMA Configuration → Acquisitions → Licenses → Manage License Terms**

This page displays a complete list of all available license terms. For each term you can configure:

| Setting | Description |
|---------|-------------|
| **License Section** | Which section this term appears in. If no section is selected, the term will not appear anywhere on the License Terms tab. |
| **Position** | A numerical value controlling the order of the term within its section |
| **Display to Public** | If enabled, library patrons can see this term when viewing a resource's license in Discovery |

### Adding a License Term to a Section

To make a term available (e.g., adding a *Remote Access* term to the *Restrictions* section):

1. Locate the appropriate term in the list (e.g., *Remote Access*).
2. Under **License Section**, select the section where it should appear (e.g., *Restrictions*).
3. Optionally set its **position** within the section.
4. Click **Save**.

---

## Verifying Your Changes

To confirm that your configuration changes are reflected:

1. Navigate to: **ALMA → Acquisitions → Acquisitions Infrastructure → Licenses**
2. Open an existing license or create a new one.
3. Go to the **License Terms** tab.

Your customizations will be visible — for example:
- The *Restrictions* section will now include the *Remote Access* term
- The *Obligations* section will appear above *Perpetual Rights* if that order was configured

---

## Summary

Configuring license terms in ALMA gives your institution precise control over how license conditions are captured and presented — both to internal staff and, optionally, to library patrons in Discovery. By managing section order, term visibility, and term placement, you can tailor the License Terms tab to reflect the structure and terminology that best matches your institution's licensing workflows.
