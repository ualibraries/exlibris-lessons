# ALMA Display Logic Rules: A Configuration Tutorial

## Overview

Display Logic Rules allow you to control which services are shown to patrons in Discovery. These services include:

- **Get It** — physical availability and request options
- **View It** — electronic full-text access
- **How to Get** — resource sharing and interlibrary loan options
- **Additional links** — any other configured patron-facing links

By configuring Display Logic Rules, you can hide specific services based on conditions you define — for example, hiding a resource sharing option when the item is already available, or suppressing a duplicate electronic collection when another source already provides full-text.

---

## Accessing Display Logic Rules

Navigate to:

**ALMA Configuration → Fulfillment → Discovery Interface Display Logic → Display Logic Rules**

This page lists all current rules.

### Managing Existing Rules

From this page you can:
- **Enable or disable** rules using the toggle slider
- Use the **Row Action** tool to **Edit**, **Duplicate**, or **Remove** a rule
- Select multiple rules and use **Bulk Actions** to apply changes to several rules at once

### Viewing a Rule

To inspect how an existing rule is built, click the **Row Action** tool and select **Edit**. You will see which service is hidden and under what conditions. Click **Save and Close** if you made changes, or **Cancel** to exit without saving.

#### Out-of-the-Box Rules

ALMA includes several pre-configured rules, such as:
- Rules that hide resource sharing services when the resource is already available to the user
- A rule that hides the purchase request option when the item is already owned by the institution

---

## Creating a New Display Logic Rule

The following example creates a rule that hides an EBSCOhost electronic collection when full-text is already available from EBSCOhost.

1. Click **Add Rule**.

2. **Select User Groups** — choose the user groups to which this rule should apply. If no user group is selected, the rule applies to **all users**.

3. **Select the service(s) to hide** — in this example, select **Full-Text**.

4. **Configure the With / Without fields** — these fields appear based on your service selection and define the conditions under which the service is hidden:
   - In the first **With** field, select **Electronic Collection**
   - In the **With Value** field, locate your specific collection (e.g., *Biomedical Electronic Collection*)

5. **Select the If Exists Service** — select **Full-Text** to trigger the rule when a full-text service is present on the page.

6. **Configure the second With field** — to prevent the collection from displaying when any full-text from a specific provider is present:
   - Select **Interface** in the next **With** field
   - Select **EBSCOhost** in the **With Value** field

   This rule will now hide the Biomedical Collection whenever the service page includes or displays any full-text from EBSCOhost.

7. Click **Add and Close**.

Your rule is now active and will suppress the specified collection under the defined conditions.

---

## Summary

Display Logic Rules give you fine-grained control over what patrons see in Discovery, preventing redundant or inappropriate service options from appearing. Rules can be tailored by user group, service type, electronic collection, and interface provider. For a full list of hideable services and additional configuration options, refer to the Knowledge Center.
