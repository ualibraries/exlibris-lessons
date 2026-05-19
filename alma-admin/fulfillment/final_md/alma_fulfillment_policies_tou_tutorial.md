# ALMA Fulfillment Policies and Terms of Use: A Configuration Tutorial

## Overview

Fulfillment in ALMA is built from three layered components:

- **Policies** — individual rules governing specific behaviors (e.g., overdue fines, maximum renewal periods, loanability)
- **Terms of Use** — combinations of policies applied together to define a complete service profile
- **Fulfillment Unit Rules** — determine which Terms of Use applies based on an item's location and the patron's situation

Together, these three components define the attributes and parameters applied whenever a patron uses the library. This tutorial covers how to configure Policies and Terms of Use.

> For information on Fulfillment Units and Rules, see the corresponding session in the Alma Essentials Training in the Knowledge Center.

---

## Accessing Policy Management

Navigate to:

**ALMA Configuration → Fulfillment → Physical Fulfillment → Advanced Policy Configuration**

This page lists all current policies. Use the **Policy Type** drop-down to filter by type.

### Managing Existing Policies

From the **Row Action** tool next to any policy, you can:
- **Edit** — modify the policy
- **Duplicate** — copy it as a starting point for a new policy
- **Delete** — remove it
- **Show Related Terms of Use** — view which Terms of Use currently use this policy

---

## Creating a New Policy

1. Click **Add Fulfillment Policy**.
2. On the first page of the wizard, select the **Policy Type** (e.g., *Is Loanable* for a loan policy).

   > For a full list of policy type descriptions, see the Knowledge Center.

3. Click **Next**.
4. Enter a **Policy Name** and optional description.
5. In the **Value** field, select the relevant value to activate the policy.

   > The available values vary depending on the policy type selected.

6. In the **Default Policy** field, choose whether this should be the default for its type. Default policies appear pre-selected in Policy drop-down lists.
7. Click **Save**.

---

## Accessing Terms of Use Management

Navigate to:

**ALMA Configuration → Fulfillment → Physical Fulfillment → Terms of Use and Policies**

This page lists all current Terms of Use. Use the **Terms of Use Type** drop-down to filter by type.

### Managing Existing Terms of Use

From the **Row Action** tool next to any Terms of Use, you can:
- **Edit** — modify it
- **Show Related Fulfillment Rules** — view the rules connected to this Terms of Use and the Fulfillment Units they apply to. Click on a rule or Fulfillment Unit title to see more detail.

---

## Creating a New Terms of Use

1. Click **Add Terms of Use**.
2. Select the **Terms of Use Type** (e.g., *Loan* for a loan Terms of Use).

   > For more information on Terms of Use types, see the Knowledge Center.

3. Click **Next**.
4. Enter a **Name** and optional description.
5. Select the **policies** to apply. If you set a policy as the default earlier, it will appear pre-selected; otherwise, choose it from the drop-down.
6. Select any remaining policies you want to include.
7. Click **Next** to review a summary.
8. Click **Save**.

Your new Terms of Use is now created with the selected policies applied.

---

## Summary

Policies and Terms of Use work together as the foundation of ALMA's fulfillment system. By creating individual policies and combining them into Terms of Use, you build the service profiles that govern how items are loaned, renewed, and managed — and those profiles are then applied to specific locations through Fulfillment Unit Rules.
