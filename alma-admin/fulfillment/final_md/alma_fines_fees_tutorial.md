# ALMA Fines and Fees: A Configuration Tutorial

## Overview

Fines and fees are charges applied to a patron's record for activities such as returning items late or losing them. In ALMA, the parameters for fines and fees are determined by the library's **Terms of Use**, in combination with **policies** and **rules**.

This tutorial explains where fines and fees are configured and how to update their settings.

> For a full explanation of how policies, Terms of Use, and rules work together, see the corresponding session in the Alma Essentials Training.

---

## Viewing Fines and Fees in Terms of Use

Navigate to:

**ALMA Configuration → Fulfillment → Terms of Use and Policies**

Each Terms of Use listed here may have policies related to fines and fees associated with it. This is where the fine amounts and behaviors are ultimately applied.

---

## Configuring Fine and Fee Behavior

Navigate to:

**ALMA Configuration → User Management → Fines, Fees → Behavior**

This mapping table lists all types of fines and fees used across your policies and Terms of Use. For each entry, you can configure:

| Field | Description |
|-------|-------------|
| **Type** | The category of fine or fee |
| **Name / Label** | Display name — *can only be changed by Ex Libris* |
| **Waivable** | Whether staff can waive this fine |
| **Manually Added** | Whether staff can manually add this fine to a patron account |
| **Auto-Generated** | Whether the system creates this fine automatically (via a rule, job, or process) |
| **Refundable** | This field has **no effect** here — configure refund behavior via the *Lost Item Replacement Fee Refund Ratio* in the loan policy |
| **Owner** | **Library** = staff must be at a circulation desk to manually add the fine; **Institution** = no desk required |

### Editing a Fine or Fee

1. Locate the fine or fee in the table.
2. Click the **Row Action** tool and select **Customize**.
3. Make the desired changes.
4. Click **Save**.

---

## Summary

Fine and fee configuration in ALMA is straightforward but spread across two areas: the Fines, Fees Behavior table controls how each type operates system-wide, while the actual amounts are set within loan policies attached to Terms of Use. Always review both locations when troubleshooting or updating your institution's fine structure.
