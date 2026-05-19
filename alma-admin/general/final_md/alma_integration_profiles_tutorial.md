# ALMA Integration Profiles: A Configuration Tutorial

## Overview

ALMA can be integrated with external systems such as:
- **Student Information Systems (SIS)** — to keep patron data synchronized
- **Enterprise Resource Planning (ERP) systems** — to synchronize invoices, orders, and funds
- **Vendor Systems** — to manage electronic holdings and ordering

These integrations are governed by **Integration Profiles**, which specify the job that runs in ALMA to handle the data transfer.

---

## Accessing Integration Profiles

Navigate to:

**ALMA Configuration → General → External Systems → Integration Profiles**

This page lists all existing integration profiles. For each profile you can see:
- **Name and Code** — unique identifiers
- **Integration Type** — the category of integration

Use the **filter** at the top to narrow the list by integration type.

### Managing Existing Profiles

From the **Row Action** tool next to any profile, you can:
- **Edit** — open and modify the profile
- **Job History** — view previous runs of this profile's job
- **Delete** — remove the profile

---

## Common Integration Profile Types

| Integration Type | Purpose |
|-----------------|---------|
| **Bursar** | Synchronize fines and fees with your Bursar's office |
| **Finance** | Synchronize invoices, orders, and funds with your ERP |
| **LDAP** | Configure ALMA staff user authentication |
| **Resolver Proxy** | Configure the proxy server for authorizing full-text access from content providers |
| **SAML** | Enable single sign-on |
| **Self-Check Machines** | Allow patrons to check out library items independently |
| **Upload Electronic Holdings** | Import electronic holdings from supported content providers |
| **Users** | Synchronize ALMA users with your SIS |

> For a complete list of integration profile types and their descriptions, see the *External Systems* document in the Knowledge Center.

---

## Editing an Existing Integration Profile: Users Example

Click on the profile name to open it. The profile contains two key tabs:

### General Information Tab
- Edit identifying details of the integration
- Configure the **SFTP connection type** — the server used for transferring files between systems

### Actions Tab
Configures the specific actions for this integration type. For a **Users** integration:

#### Imports Section
- Import new users from the SIS by configuring the relevant parameters and clicking **Run**
- This option runs manually only and cannot be scheduled

#### Synchronize Section
- Update existing users, matched by a user ID of your choice
- Matched records are **overwritten** in ALMA
- Choose whether to **add** or **reject** unmatched records
- Set a **schedule**: every 6 hours, daily, weekly, or not scheduled

> For details on all Users integration options, see the *Student Information Systems* document in the Knowledge Center.

Click **Save** when done editing.

---

## Creating a New Integration Profile

1. Click **Add Integration Profile**.
2. Select the **Integration Type** (e.g., *Upload Electronic Holdings*).
3. Enter a **unique Code** for the profile.
4. For types like Upload Electronic Holdings, select the **provider** from the available list.
5. Enter an optional **description**.
6. Click **Next**.

On the second step of the wizard:
- Ensure the profile **Status** is set to **Active**
- Enter any parameters specific to this integration type (e.g., for eBook Central: Site ID, Vendor, PO Line Owner Library)
- Optionally **run the import now**, or configure it to run on a schedule

Click **Save**. Your new integration profile is created and — if active — will run according to its configured schedule.

---

## Technical Resources for Integrations

For technical specifications related to data transfer between ALMA and external systems — including input/output file formats — visit the **Ex Libris Developer Network**:

**developers.exlibrisgroup.com → Alma → Standards and Integrations**

Here you will find:
- Industry standards supported by ALMA
- Training videos for specific integration types
- Technical specifications for each integration type
- Your ALMA domain name (required to access ALMA via API)

---

## Summary

Integration profiles are the control center for keeping ALMA in sync with the rest of your institution's systems. By managing existing profiles and creating new ones, you can automate the flow of user, financial, and holdings data between ALMA and your SIS, ERP, and vendor systems — reducing manual effort and ensuring data consistency across platforms.
