# ALMA Purchasing and Invoice Rules: Automating Acquisitions Workflows

## Overview

ALMA allows you to automate key steps in your acquisitions workflows using three types of rules:

- **Purchasing Review Rules** — automate the Review step of the purchasing workflow
- **Invoice Review Rules** — automate the Review step of the invoicing workflow
- **Invoice Approval Rules** — automate the Approval step of the invoicing workflow

This tutorial covers how to configure each of these rule types.

---

## The Purchasing Workflow

The full purchasing workflow in ALMA consists of these steps:

**Create PO Line → Validation → Review → Packaging → Approval → Receiving**

Several of these steps can be automated. This tutorial focuses on automating the **Review** step using Purchasing Review Rules.

---

## Purchasing Review Rules

Purchasing Review Rules determine whether automatically created PO Lines are sent to **manual review** or proceed **directly to the next step**.

Navigate to:

**ALMA Configuration → Acquisitions → Purchase Orders → Purchasing Review Rules**

### How ALMA Evaluates Rules

ALMA evaluates rules in this order:

1. **Default Review Rule** — this rule has no criteria; it is simply set to True or False.
   - If **True**: all PO Lines are sent for manual review.
   - If **False**: ALMA proceeds to evaluate institution rules.
2. **Institution Rules** (evaluated in order, top to bottom):
   - If a rule applies to the PO Line and its result is **True**: the PO Line is sent for manual review.
   - If a rule applies and its result is **False**: the PO Line goes straight to the next step.
   - If **no rule applies**: the PO Line goes straight to the next step.

### Creating a Purchasing Review Rule

Click **Add Rule** and fill in the following:

- **Name** and optional **Description**
- **Input Parameters — Assertion Code In**: the criteria to evaluate. Examples:
  - *Duplicate Active Orders* — the item already has an active order
  - *Fund is Over-Encumbered*
  - *Already Has Inventory* — the item already exists in your inventory

  > A full list of assertion codes is available in the *Configuring Purchasing Review Rules* document in ALMA Online Help.

- **Acquisition Methods**: select which methods this rule applies to (e.g., *Purchase*)
- **Vendor** *(optional)*: limit the rule to a specific vendor
- **PO Line Types**: select which line types this rule applies to (e.g., *Print Book One Time*)
- **Source Types**: select how the PO Line was generated (e.g., *Purchase Request*). Select **Any** to include all source types.
- **Output Parameters**:
  - **True** — send the PO Line to manual review
  - **False** — send the PO Line straight to the next step

Click **Save** when done.

### Managing Rules

From the Purchasing Review Rules list, you can:
- **Reorder** rules using the up and down arrows
- **Enable or disable** individual rules (disabled rules are ignored during evaluation)
- **Edit**, **Duplicate**, or **Delete** rules

---

## The Invoicing Workflow

The invoicing workflow in ALMA consists of these steps:

**Creation → Review → Approval → Payment**

- The **Review** step can be automated using **Invoice Review Rules**
- The **Approval** step can be automated using **Invoice Approval Rules**

---

## Invoice Review Rules

Invoice Review Rules determine whether invoices are sent for **manual review** or proceed **directly to approval**.

Navigate to:

**ALMA Configuration → Acquisitions → Invoices → Invoice Review Rules**

### How ALMA Evaluates Invoice Review Rules

The logic mirrors Purchasing Review Rules:
- A **Default Review Rule** can be set to Always True or Always False.
  - **Default: False** — all invoices go straight to approval unless an institution rule specifies otherwise.
  - If set to **True** — all invoices are sent to manual review.
- Institution rules are evaluated in order if the default is False.

### Creating an Invoice Review Rule

Click **Add Rule** and configure:

- **Name** and optional **Description**
- **Assertion Code**: the condition to evaluate. Example: *Invoice Using Different Vendor Than PO Line*

  > A full list of assertion codes is in the *Configuring Invoice Review Rules* document in ALMA Online Help.

- **Vendor** *(optional)*: limit the rule to a specific vendor
- **Invoice Line Numbers**: use a regular expression to match specific invoice line numbers, or enter `*` to match all
- **Invoice Creation Form** *(optional)*: limit the rule to invoices created in a specific way (e.g., manually created invoices only)
- **Output Parameters**:
  - **True** — send the invoice to manual review
  - **False** — send the invoice straight to approval

Click **Save** when done.

---

## Invoice Approval Rules

Invoice Approval Rules determine whether invoices require **manual approval** or proceed **directly to payment**.

Navigate to:

**ALMA Configuration → Acquisitions → Invoices → Invoice Approval Rules**

### How They Work

- If a rule evaluates to **True**: the invoice is sent for manual approval.
- If a rule evaluates to **False**: the invoice is sent straight to payment.

Configuration follows the same structure as Invoice Review Rules. A full list of available assertion codes is available in the *Configuring Invoice Approval Rules* document in ALMA Online Help.

---

## Summary

| Rule Type | Workflow Step Automated | Location |
|-----------|------------------------|----------|
| Purchasing Review Rules | PO Line Review | Configuration → Acquisitions → Purchase Orders |
| Invoice Review Rules | Invoice Review | Configuration → Acquisitions → Invoices |
| Invoice Approval Rules | Invoice Approval | Configuration → Acquisitions → Invoices |

By thoughtfully configuring these three rule types, you can significantly reduce the manual effort required in your acquisitions workflows — routing only the exceptions that genuinely need human attention to staff queues.
