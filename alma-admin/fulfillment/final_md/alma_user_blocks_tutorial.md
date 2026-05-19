# ALMA User Blocks: A Configuration Tutorial

## Overview

Blocks restrict patrons from using library services — such as borrowing or renewing items — when certain conditions apply, such as having outstanding fines, too many overdue items, or a suspended account status.

Configuring a user block in ALMA is a two-step process:

1. **Create a User Block Description** — defines the type and reason for the block
2. **Create a User Block Definition** — applies the description and sets the rules for who can override it and what actions it restricts

---

## Step 1: Configure User Block Descriptions

Navigate to:

**ALMA Configuration → Fulfillment → Patron Configurations → User Block Description**

This table lists all current block descriptions with their codes and descriptions (e.g., *Too Many Claimed Returned Items*, *Must Meet with Academic Advisor*).

### Managing Existing Descriptions

- **Edit** any row directly in the table
- Use the **Row Action** tool and select **Delete** to remove a description

### Adding a New Block Description

1. Click **Add Row**.
2. Enter a **Code** — a unique identifier for this block type.
3. Enter a **Description** — a human-readable explanation of the block.
4. Optionally, check **Default** — this sets the description as the pre-selected option in the block definitions creation menu.
5. Click **Add Row** to confirm.
6. Click **Save**.

---

## Step 2: Configure User Block Definitions

Navigate to:

**ALMA Configuration → Fulfillment → Patron Configurations → User Block Definitions**

This mapping table links block descriptions to their behavioral rules.

### Adding a New Block Definition

1. Click **Add Row**.
2. Enter an **ID** for the definition.
3. Set the **Type** to *User*.
4. Select the **Description** you created in Step 1 — this tells the definition which block type and reason to apply.
5. Configure the remaining fields:

#### Override Permissions

Choose who is allowed to override this block:

| Option | Who Can Override |
|--------|-----------------|
| **All** | Any circulation desk operator |
| **None** | The block cannot be overridden |
| **CircDesk** | Circulation desk managers only |
| **Operator** | Circulation desk managers and operators (but not operators with limited permissions) |

#### Blocked Action

Choose which library services are restricted:

| Value | Services Blocked |
|-------|-----------------|
| **1** | Loans only |
| **2** | Loans and renewals |
| **3** | Loans, renewals, and hold requests |

#### Network Block

Select whether this block will be **copied** when creating or refreshing a linked account (relevant for network zone configurations).

6. Click **Add Row** to confirm.
7. Click **Save**.

---

## Summary

Once both the description and definition are configured, the block can be applied to patron accounts. For example, a block created for suspended students will prevent them from checking out or renewing items until the block is resolved or overridden by an authorized staff member.
