# ALMA Fiscal Period Closure and Rollover: A Tutorial

## Overview

Closing a fiscal period in ALMA requires running three sequential rollover jobs to carry forward your financial and ordering data into the next fiscal period:

1. **Rollover Ledgers** — copies ledgers from the closing fiscal period to the next
2. **Rollover PO Lines** — copies purchase order lines to the next fiscal period
3. **Rollover Resource Sharing Requests** — copies resource sharing transactions to the next fiscal period *(only relevant for institutions using resource sharing)*

> **Required role:** You must have the **Fiscal Period Manager** role to perform these workflows. For complete instructions, refer to the *Fiscal Period Closure* document in the Knowledge Center.

---

## Managing Fiscal Periods

Fiscal periods are managed at:

**ALMA Configuration → Acquisitions → General → Fund and Ledger Fiscal Period**

This page displays all existing fiscal periods in ALMA. New fiscal periods are **created automatically** when you run the Rollover Ledgers job — you do not need to create them manually.

---

## Step 1: Rollover Ledgers

Navigate to:

**ALMA → Acquisitions → Advanced Tools → Rollover Ledgers**

This page shows all previous runs of the Rollover Ledgers job and their statuses.

### Adding a Rollover Job

Click **Add Job** and fill in the parameters:

#### Create Allocation From

Select how funds will be carried into the new fiscal period:

| Option | Behavior |
|--------|----------|
| **None** | No allocations are created for the new fiscal period |
| **Allocation Balance** | Copies the old allocation amount to the new ledger |
| **Cash Balance** | Populates the new ledger's allocation with the old ledger's cash balance |
| **Both** | Copies both the allocation and cash balances to the new ledger |

#### FPC Factor

If you selected an allocation option, you may enter an **FPC (Fiscal Period Change) factor** — a percentage increase or decrease applied to the new allocation (e.g., entering `1` increases the new allocation by 1%).

#### Additional Parameters

- **Ledger scope** — rollover all ledgers, or limit to a specific ledger
- **New ledger status** — set new ledgers to **Draft** (functionally inactive) or **Active**
- **Action** — choose to **copy** ledgers to the new fiscal period, or **delete** old ledgers (only ledgers with no encumbrance will be deleted)
- **Source period** — rollover from the current or previous fiscal period to the next one in line

When finished, click **Add and Close**. The job will appear as pending. Click **Refresh** to monitor progress. When complete, the status will show *Completed Successfully* along with the number of ledgers rolled over. Full details are available in the job report.

---

## Step 2: Rollover PO Lines

Navigate to:

**ALMA → Acquisitions → Advanced Tools → Rollover PO Lines**

The process is similar to the ledger rollover.

### Adding a Rollover Job

Click **Add Job** and fill in the parameters:

- **Library scope** — rollover PO lines for the entire institution, or limit to selected libraries
- **Specific PO line** — optionally limit the rollover to a single PO line
- **Check over encumbrance** — if selected, ALMA enforces over-encumbrance rules for the fund or ledger during rollover

### Run in Report Mode First

> **Best practice:** Before running a live PO line rollover, first run the job in **Report Mode**. This generates a report identifying any errors that need to be resolved, simulating the rollover without making any actual changes to the repository.

When finished entering parameters, click **Add and Close**. Monitor the job status by refreshing the page.

---

## Step 3: Rollover Resource Sharing Requests

*(Skip this step if your institution does not use resource sharing in ALMA.)*

Navigate to:

**ALMA → Acquisitions → Advanced Tools → Rollover Resource Sharing Requests**

Click **Add Job**, fill in the rollover parameters as desired, and click **Add and Close**.

When this job completes, all three fiscal period rollover jobs are finished and your institution is ready to operate in the new fiscal period.

---

## Summary

Fiscal period closure in ALMA is a structured three-job process. Running the jobs in order — ledgers first, then PO lines, then resource sharing requests — ensures your financial data, purchase orders, and resource sharing transactions are carried forward correctly. Always use Report Mode for the PO line rollover to catch errors before committing changes.
