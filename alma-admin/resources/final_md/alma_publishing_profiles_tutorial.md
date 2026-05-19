# ALMA Publishing Profiles: A Setup Tutorial

## Overview

Publishing profiles enable your institution to send information about bibliographic or authority records from ALMA to other systems. Common publishing destinations include:

- External catalogs (e.g., OCLC)
- Primo
- Google Scholar
- RSS feeds
- And more

While the setup process varies depending on the type of publishing, most profiles share a common set of steps:

1. **Configuring the profile** — defining how and where information will be published
2. **Scheduling the job** — setting when the publishing job will run
3. **Identifying the records** — either by creating a set or marking individual records

This tutorial walks through the setup process using **publishing to OCLC** as the primary example.

---

## Accessing Publishing Profiles

Navigate to:

**ALMA → Resources → Publishing → Publishing Profiles**

There are two tabs:

- **Institution tab** — all publishing profiles available at your institution
- **Community tab** — publishing profiles created by other institutions that you can copy

---

## Choosing or Creating a Profile

To create a profile from scratch, select **Add Profile** and choose one of the following:
- **General Profile**
- **Research General Profile**
- **RSS**

Each type requires somewhat different parameters.

However, ALMA comes with several of the most common publishing profile types pre-loaded. It is likely that the type of profile you need is already listed — and can simply be modified for your institution's specific needs.

> **Important:** Do **not** modify the profile titled *Publish Electronic Records to Central Discovery Index*. This profile has been configured by your implementation team to populate Primo correctly.

---

## Configuring the OCLC Publishing Profile

Locate the profile **Publish Bibliographic Record, Data Sync, to OCLC**:

1. Click the **Row Action** button and select **Edit**.
2. After the name and description fields, enter your **OCLC institution symbol** and any other required information.

### Publishing Mode

Choose the appropriate publishing mode based on your institution's situation:

| Scenario | Mode to Use |
|----------|-------------|
| Previously published to OCLC with an old ILS and migrating to ALMA | Start with **Baseline**, then switch to **Incremental** |
| Publishing to OCLC for the first time, or republishing all records by agreement with OCLC | Use **Full**, then switch to **Incremental** |

- **Baseline Publishing Mode** — run this **once**, immediately after Go Live and before any cataloging in ALMA.
- **Full Publishing Mode** — use when starting fresh or republishing everything.
- **Incremental Publishing Mode** — publishes only changes on a regular, ongoing basis. Switch to this after your initial baseline or full publish.

### Status

Set **Status** to **Active** for the profile to function.

---

## Scheduling the Publishing Job

1. Click **Edit Scheduling**.
2. Choose the **frequency** and **timing** for the scheduled publishing job.

---

## FTP Configuration

1. Choose the **FTP configuration**.
2. Enter the **subdirectory**.

> If you are unsure what to enter here, contact OCLC directly for guidance.

---

## Identifying Records to Publish

How records are identified for publishing depends on the profile type:

- **RSS publishing profiles** — you must create a **set of records** and input the set name into the profile.
- **OCLC and many other profile types** — records are **marked for publishing** individually or in bulk.

### Marking an Individual Record

1. Open the record in the **Metadata Editor**.
2. Select **Record Actions → Set Management Tags → Export to WorldCat**.
3. Choose one of the following options:
   - **Don't Publish**
   - **Publish Holdings Only**
   - **Publish Bib**
4. Select the option appropriate for your publishing profile (e.g., *Publish Bib* for OCLC).

Selecting either publish option will include the record the next time the Publishing to OCLC job runs.

> **Force Export to WorldCat** — use this option to publish a record **immediately**, without waiting for the scheduled job to run.

### Marking Records in Bulk

1. **Create a set** of the records you want to mark.
2. Run the **Set Management Tags** job.
3. Check the box for **Synchronize with OCLC**.
4. In the dropdown, choose the appropriate option:
   - **Publish Bib**
   - **Publish Holdings Only**
   - **Don't Publish**

> For instructions on creating a set or running a job, refer to the **Knowledge Center**.

---

## Saving Your Changes

After making any changes to a publishing profile, always click **Save** before exiting.

---

## Summary

Setting up a publishing profile in ALMA involves configuring the profile parameters, scheduling the job, and ensuring the right records are marked for publishing. While the OCLC workflow is covered here, each publishing destination has its own specific requirements. For details on other publishing profile types, refer to **ALMA Online Help**.
