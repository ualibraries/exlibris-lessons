# Primo VE Labels and My Library Activity: A Configuration Tutorial

## Overview

**Labels** are the words and phrases displayed in the Primo VE user interface — buttons, facets, availability statements, and more — that are not part of bibliographic records. They are also used to translate the interface into different languages. As an administrator, you can customize any label.

In addition, you can configure what information patrons see on their **My Library Activity** page when they log in to Discovery.

---

## Accessing Labels

Navigate to:

**ALMA → Discovery → Display Configuration → Labels**

This loads all code tables, which group labels together by function. You can search by **Code** or **Description**.

---

## Finding and Customizing a Label by Description

1. Set the search type to **Description**.
2. Enter the label text as it currently appears in Primo VE (e.g., *Tweak Your Results*).
3. Click **Search**.
4. The relevant table will appear in the results.
5. Click the **Row Action** tool and select **Customize**.
6. Within the table, search for the label again.
7. Click **Customize** next to the label.
8. Update the text in the **Description** column.
9. Click **Customize** to save.

The updated label will appear immediately in Primo VE.

---

## Finding a Label by Code (When Description Search Returns Multiple Tables)

If a description search returns multiple tables, you need the label's unique **code** to find the right one.

### How to Find a Label's Code

1. Go to your Primo VE site.
2. Append the following parameter to the URL:

   `?debugLabels=true`

3. This replaces all interface labels with their codes instead of display text.
4. Locate the element you want to change — note its code.

   > **Note:** Codes cannot be changed, only the descriptions they display.

5. Return to ALMA Labels, set the search type to **Code**, enter the code, and click **Search**.
6. Open the correct table and customize the label as described above.

### Searching for Labels in Multiple Languages

If your Primo VE site supports multiple languages:
1. Use the **language filter** when searching for the table and for the label.
2. Adjust the translated label for each language as needed.

---

## Configuring the My Library Activity Page

When patrons log in to Discovery, they see their **My Library Activity** page. Four areas can be configured here:

Navigate to:

**ALMA Configuration → Discovery → Library Card Configurations**

### 1. Loans Detailed Display
Configure which lines appear in the detailed view of a loan and the order they display in.

**Example additions:** Year of the loan, Main Location Name.

Click **Save** after making changes.

### 2. Loans Brief Display
Configure the two lines shown in the brief summary of a loan. Use the **drop-down menus** in each value column to choose what information appears.

**Example additions:** Loan Date, Loan Status (on line 1).

Click **Save** after making changes.

Changes are immediately visible in Primo VE upon refresh.

### 3. Payment Link Configuration
Enable the **Pay Fine** link to display in the patron's overview under Fines and Fees.

### 4. Personal Details Configuration
Configure which personal information displays under **Settings → Personal Details** in Primo VE, such as additional email addresses.

As an administrator, you can also allow patrons to set preferences such as:
- Saving search history
- Selecting the default UI language
- Updating their credentials

> For more information on each section, see the Knowledge Center.

---

## Summary

Label customization lets you tailor the language of the Primo VE interface to match your institution's voice. The My Library Activity configuration gives you control over exactly what loan and personal information patrons see when they log in. Both are managed from within ALMA configuration and take effect immediately.
