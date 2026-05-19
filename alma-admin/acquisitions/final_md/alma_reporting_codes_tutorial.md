# ALMA Acquisitions Reporting Codes: A Configuration Tutorial

## Overview

When generating Analytics reports on acquisitions, ALMA provides standard PO Line attributes such as the PO Line identifier, status, and vendor name. In addition, ALMA offers **five generic PO Line attributes** called **Reporting Codes**, which you can configure for any custom categorization your institution needs.

**Examples of reporting code uses:**
- Reporting Code 1: Media type (Book, E-Book, E-Journal, etc.)
- Reporting Code 2: Genre
- Reporting Code 3: Library initiative (Religious Tolerance, Campus Safety, etc.)
- Reporting Codes 4–5: Any additional custom categories

Reporting codes can also be used to retrieve data about **invoice lines**. By default, invoice lines inherit the reporting code from their linked PO Line, but this can be manually overridden when editing an individual invoice line.

In this tutorial, you will learn how to:
- Configure reporting codes
- Add reporting codes to a PO Line
- Create an Analytics report that displays reporting code data

---

## Configuring Reporting Codes

Navigate to:

**ALMA Configuration → Acquisitions → Purchase Orders → Acquisition Method**

Under **Purchase Orders**, select one of the five available reporting codes to configure (e.g., *Reporting Code 4*).

### Adding a Reporting Code Value

1. Click **Add Row**.
2. Enter a **Code** and an optional **Description** (e.g., Code: `REL_TOL`, Description: *Religious Tolerance*).
3. Optionally, check the box to make this the **default value** that appears pre-selected in the PO Line drop-down list.
4. Click **Add Row** to confirm.
5. Repeat for each additional value (e.g., *Campus Safety*).
6. Click **Save** when all codes have been entered.

---

## Adding Reporting Codes to a PO Line

1. In ALMA, search for a PO Line and open it for editing.
2. On the **Purchase Order Line Details** page, scroll down to the **Reporting Codes** section.
3. Use the drop-down lists to select the appropriate reporting code value for each configured reporting code.
   - Some reporting codes may be empty if they have not yet been configured or are not applicable to this PO Line — these can be filled in later.
4. Save the PO Line.

---

## Creating an Analytics Report by Reporting Code

Navigate to:

**ALMA → Analytics → Design Analytics**

1. Click **Create → Analysis**.
2. For the **Subject Area**, select **Purchase Requests**.
3. Under **PO Line**, select the attributes you want to include:
   - *PO Line Identifier*
   - *PO Line Title*
   - *Reporting Code 4th* (or whichever reporting code you configured)
   - *Reporting Code Description 4th* (the text description corresponding to each code)
4. Add a **filter** on the reporting code field:
   - Set the condition so the field **is not null** — this ensures only PO Lines with this reporting code assigned appear in the report.
5. Open the **Results** tab to view the report.

The report will display PO Lines with the reporting code value in one column and its description in another.

---

## Summary

Reporting codes give purchasing staff a flexible way to tag PO Lines with institution-specific categories, and give administrators a powerful tool for slicing acquisitions data in Analytics reports. With up to five configurable codes per PO Line — and the ability for invoice lines to inherit or override those codes — reporting codes can support a wide range of analytical and administrative needs.
