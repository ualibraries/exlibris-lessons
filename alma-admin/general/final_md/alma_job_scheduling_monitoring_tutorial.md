# ALMA Job Scheduling and Monitoring: A Tutorial

## Overview

ALMA uses jobs to automate a wide range of processes — from sending overdue notices to harvesting usage statistics. Understanding how to schedule and monitor these jobs is an essential part of ALMA administration.

In this tutorial, you will learn how to:
- Understand the types of jobs in ALMA
- Schedule fulfillment and acquisitions jobs
- Monitor job status across scheduled, running, and completed jobs
- Add a job status widget to your ALMA homepage

---

## Types of Jobs in ALMA

| Job Type | Description |
|----------|-------------|
| **Manual** | Run on demand by library staff |
| **Scheduled (Ex Libris)** | Run automatically on a schedule set by Ex Libris; cannot be changed by the institution |
| **Scheduled (Institution)** | Run automatically on a schedule configured by ALMA administrators |

Many jobs can be run both manually and on a schedule.

---

## Scheduling Fulfillment Jobs

Navigate to:

**ALMA Configuration → Fulfillment → General → Fulfillment Jobs Configuration**

This page lists all fulfillment-related scheduled jobs (e.g., *Borrowing Activity Report*, *Send Overdue Notices*).

### Configuring a Job

For each job, you can:
- Set it to **Active** (runs on schedule) or **Inactive** (does not run automatically, but may still be run manually)
- Open the **Schedule** dropdown and select from the available options (e.g., weekly on a selected day, monthly on a selected date, or not scheduled)
- Click **Run Now** to trigger a manual run where available
- Configure any **job-specific settings** (e.g., for the Anonymization job, choose which fulfillment activities will have identifying user information scrubbed)

> Available schedule options may vary by job type and by your region and settings.

Click **Save** when done.

---

## Scheduling Acquisitions and Resource Management Jobs

Acquisitions jobs are configured at:

**ALMA Configuration → Acquisitions → General → Jobs Configuration**

This includes jobs such as the **PO Line Package** job and the **Sushi Harvesting** job.

Resource Management jobs are available on a similar configuration page within that functional area.

---

## Monitoring Jobs

Navigate to:

**ALMA → Admin → Manage Jobs and Sets → Monitor Jobs**

This section has three tabs:

### Scheduled Tab
Displays all upcoming scheduled jobs, whether configured by library staff or Ex Libris.

For each job you can see:
- Whether it is **Active**
- Its **schedule** and **next run time**

From the **Row Actions** menu, you can:
- **View Job History** — see previous runs
- **Add Subscribers** — add yourself and other users to receive email notifications when this job runs

Use the **category filter** (e.g., Fulfillment) to narrow the list.

### Monitor Jobs Running Tab
Shows the progress of all currently running jobs, including both scheduled and manually triggered jobs.

### Monitor Jobs History Tab
Lists all completed jobs. Filter by:
- **Job category**
- **Job status** (success, errors)
- **Submit date range** (e.g., all jobs run last month)

From **Row Actions**, you can:
- **Pull up the Job Report** — detailed information about the job run
- **View Events** — see any error messages raised during runtime

---

## Adding the Scheduled Job Status Widget to Your Homepage

A convenient way to keep an eye on job health is to add the **Scheduled Job Status** widget to your ALMA dashboard.

1. From the ALMA homepage, click the **+ (plus) icon** in the top right of the dashboard.
2. Select **Scheduled Job Status** from the widget list.
3. Close the Manage Widgets dialog.
4. **Drag and drop** the widget to your preferred position on the dashboard.

### Using the Widget

The widget displays the status of scheduled jobs for the **last five days**.

- Use the **date** and **job category** selectors to filter the view
- Color-coded indicators show **successes** and **failures** at a glance
- Click the **arrow** next to a job category to be redirected to the **Monitor Jobs History** tab, pre-filtered to show the jobs in that category — particularly useful for investigating failures

---

## Summary

Effective job management keeps your ALMA environment running smoothly and your data current. By scheduling the right jobs, monitoring their outcomes, and using the homepage widget for at-a-glance visibility, you can catch issues early and ensure that automated processes are performing as expected.
