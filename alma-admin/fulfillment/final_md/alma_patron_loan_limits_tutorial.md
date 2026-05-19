# ALMA Patron and Loan Limits: A Configuration Tutorial

## Overview

ALMA allows you to configure two types of limits that restrict patron borrowing activity:

- **Patron Limits** — set maximum thresholds for fines, overdue items, requests, etc., before a patron's account is blocked
- **Loan Limits** — restrict how many items a patron can have checked out simultaneously, based on user group, item policy, material type, location, and other criteria

---

## Configuring Patron Limits

Navigate to:

**ALMA Configuration → Fulfillment → Patron Configurations → Patron Limits**

This page lists all user groups and their current patron limit thresholds (e.g., Graduate Students, Undergraduate Students, Faculty, Guests).

### Adding a New Set of Patron Limits

1. Click **Add Row**.
2. Select the **User Group** (e.g., *High School Students*).
3. Enter the **maximum amounts** for each limit field you want to enforce.

   > If a field is left blank, no limit will be applied to that category.

4. Click **Add Row** to confirm.
5. Click **Save**.

To remove a set of patron limits, click the **Row Action** tool next to the row and select **Delete**, then save.

> For information on creating user groups, see the corresponding session in the Alma Essentials Training in the Knowledge Center.

---

## Configuring Loan Limits

Navigate to:

**ALMA Configuration → Fulfillment → Patron Configurations → Loan Limits**

This page lists all current loan limit rules.

> **Note:** Loan limit rules can only be configured at the **institution level**.

### Managing Existing Rules

- Use the **toggle** to enable or disable individual rules
- Use the **arrow buttons** to reorder rules — ALMA assigns a patron the **first rule for which they meet all criteria**
- Use the **Row Action** tool to **Edit**, **Duplicate**, or **Delete** a rule

### Editing a Rule

Click **Edit** to open the rule. You can modify:
- **Input Parameters** — conditions based on library location, item policy, material type, user group, and more
- **Output Parameters** — the loan limit applied when input conditions are met

Click **Save** if you made changes.

### Creating a New Loan Limit Rule

1. Click **Add Rule**.
2. Enter a **Name** (required) and optional description.
3. Add **Input Parameters** to define who and what the rule applies to. Examples:
   - **User Group**: *High School Students*
   - **Item Policy**: *2-Week Loan*
4. Set the **Output Parameter** — the maximum number of items the patron can check out when the input conditions are met (e.g., *5 items*).
5. Click **Save**.

---

## Example: High School Student Limits

| Configuration | Setting |
|---------------|---------|
| User Group | High School Students |
| Patron Limit | Configured thresholds for fines, overdue items, etc. |
| Loan Limit Rule Input | User Group = High School Students; Item Policy = 2-Week Loan |
| Loan Limit Rule Output | Maximum 5 items simultaneously |

---

## Summary

Patron limits and loan limits work in tandem to manage how much library activity a patron can accumulate before being blocked or restricted. Patron limits set account-level thresholds, while loan limit rules apply granular checkout caps based on specific combinations of user group, item type, and location.
