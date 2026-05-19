# ALMA Acquisition Methods: Configuration Tutorial

## Overview

ALMA supports several acquisition methods for ordering resources, such as Purchase, Gift, and Exchange. When a purchasing operator manually creates a PO Line, they select the relevant acquisition method from a drop-down list — or accept the configured default.

As an administrator, you control which acquisition methods appear in that list and which is set as the default.

In this tutorial, you will learn how to:
- Configure which acquisition methods are available for your institution
- Understand the behavior and purpose of each acquisition method

---

## Configuring Acquisition Methods

Navigate to:

**ALMA Configuration → Acquisitions → Purchase Orders → Acquisition Method**

This page displays all available acquisition methods and their current status.

### Configuration Options

For each method you can:
- **Enable** it to make it appear in the PO Line drop-down list
- **Disable** it to remove it from the list
- Edit the **Description** column to set the text label as it will appear in the drop-down

You must also select **one method as the default** — this is the value pre-selected when a PO Line is created.

> **Note:** You cannot add, edit the method codes, or delete acquisition methods — only enable, disable, and relabel them.

When finished, click **Save**. The drop-down list in PO Lines will update to reflect your configuration.

> **Note:** Existing PO Lines are not affected by changes to this configuration.

---

## Acquisition Methods Reference

### Methods That Require Payment

| Method | Description |
|--------|-------------|
| **Purchase** | Standard purchase of a resource from a vendor |
| **Vendor System** | Used when purchasing via an external vendor system; does not send PO Lines to the vendor — packages them into POs and marks them as sent until received or activated |
| **Approval Plan** | Used when a vendor sends resources they determine are appropriate to your institution in EOD (Electronic Order Data) format; behaves identically to Vendor System |

### Methods That Do Not Require Payment

The following methods all order items **without requiring payment**. They behave identically in ALMA's workflows but appear differently in reports, making it important to choose the correct one for accurate analytics:

| Method | Description |
|--------|-------------|
| **Legal Deposit** | For governments and national libraries that receive copies at no charge from publishers or vendors |
| **Gift** | The resource is granted as a gift from a vendor or donor to the institution |
| **Technical** | For service subscription orders without inventory, or items migrated from an external system; often used for multi-part orders where one payment covers multiple resources |
| **Depository** | Used when your institution hosts government publications and makes them freely available |
| **Exchange** | Used when your institution exchanges resources with another institution |

### Send Letter vs. No Letter Variants

Each acquisition method has **two versions**:
- One that **sends a letter to the vendor**
- One that **does not**

By default, one variant of each pair is disabled. You may enable both variants if you want staff to be able to choose either option from the drop-down list.

---

## Summary

Configuring acquisition methods ensures that your PO Line drop-down reflects only the methods your institution actually uses, reducing confusion for purchasing staff. Understanding the behavioral differences between methods — particularly which ones require payment and how Vendor System and Approval Plan handle PO packaging — also helps ensure your acquisitions data is accurate in Analytics reports.
