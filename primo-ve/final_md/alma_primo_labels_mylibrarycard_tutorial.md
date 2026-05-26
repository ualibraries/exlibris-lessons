# Primo VE Labels and My Library Card Configuration: A Tutorial

## Overview

**Labels** are the words and phrases that appear in the Primo VE user interface — alert messages, facets, availability statements, button text, and more. They are also used to translate the interface into different languages. As an administrator, you can customize any label to match your institution's preferred terminology.

In addition, you can configure what patrons see on their **My Library Card** page when they log in to Discovery.

---

## Accessing Labels

Navigate to:

**ALMA → Discovery → Display Configuration → Labels**

This loads all label code tables, grouped by function. You can search for a label by:
- **Code** — the internal identifier used in the interface
- **Description** — the text as it appears to users

---

## Finding the Right Label to Customize

For common labels, a description search is straightforward. However, if multiple tables return results for a description search, you need to identify which table contains the specific label you want.

### Finding a Label Code Using Browser Inspector

If you know where a label appears in Primo VE but not its code:

1. Go to the page in Primo VE where the label is displayed.
2. **Right-click** on the element and select **Inspect** (Chrome browser recommended).
3. If you did not click precisely on the right element, use the **arrow selection tool** in the inspector to click the correct element.
4. In the HTML code, look for the attribute `translate=` — the value that follows is the label code.

   **Example:** The *Allow Saving My Search History* toggle has the code `inui.mypref.label.savehistory`.

5. Return to ALMA Labels, change the search type to **Code**, enter the code you found, and click **Search**.
6. The correct label table will appear in the results.

### Customizing a Label

1. From the search results, open the Row Action tool for the relevant table and select **Customize**.
2. Locate the specific label in the table.
3. Open its Row Action tool and select **Customize** (first time) or **Edit** (if previously configured).
4. Use the **toggle** to deactivate a label if needed, or update its value.
5. Click **Save**.

> For more information on modifying labels, see the Knowledge Center.

---

## Configuring the My Library Card Page

The **My Library Card** page is what patrons see when they log in to Discovery. There are four configurable areas, all found at:

**ALMA Configuration → Discovery → Library Card Configurations**

### 1. Loans Detail Display
Configure what information appears in the detailed view of a loan, including:
- Which lines are displayed
- The order in which lines appear

### 2. Loans Brief Display
Configure the brief summary shown for each item in a patron's account. There are two lines available, each with a drop-down to select what information is displayed.

Click **Save** after making changes.

### 3. Payment Link Configuration
Enable or configure the **Pay Fine** link that can appear in My Library Card.

> For configuration details, see the Knowledge Center.

### 4. Personal Details Configuration
Configure what information is shown on the **Personal Details** tab in My Library Card — for example, whether additional email addresses are displayed.

> For more information on each section, see the Knowledge Center.

---

## Summary

Label customization lets you align the Primo VE interface with your institution's voice and terminology, while My Library Card configuration gives you control over what account information patrons can see and manage. Together, these tools help create a more intuitive and locally relevant discovery experience.
