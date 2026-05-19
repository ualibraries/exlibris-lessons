# Introduction to ALMA Administration

## Overview

This tutorial introduces the foundational concepts of ALMA administration, including administrator roles, the configuration interface, and key online resources available to support your work as an ALMA administrator.

---

## Administrator Roles in ALMA

An ALMA administrator is any user assigned one or more administration roles. Key roles include:

| Role | Description |
|------|-------------|
| **General System Administrator** | Broad system-wide configuration access |
| **Acquisitions Administrator** | Configure acquisitions-related settings |
| **Analytics Administrator** | Configure Analytics objects and settings |
| **Catalog Administrator** | Configure cataloging and metadata settings |
| **Fulfillment Administrator** | Configure fulfillment and circulation settings |
| **Repository Administrator** | Configure repository and resource management settings |

> **Important:** Administrator roles allow users to *configure* ALMA. They do not typically enable day-to-day workflows.

### Read-Only vs. Full Access

An admin role can be set to **read-only**, which means the user can view — but not edit — configurations for that subject area.

To change this:
1. Go to the user's roles.
2. Click **Role Actions → Edit**.
3. Check or uncheck the **Read-Only** checkbox as needed.
4. Click **Save Role**.

### Superuser Roles

Two roles should be treated with special caution:

- **General System Administrator**
- **User Administrator**

Both roles allow users to assign themselves any other role in ALMA, giving them access to all configuration areas. Grant these roles only to trusted individuals.

> For a complete list of roles and their associated privileges (Role Privileges), refer to the ALMA documentation.

---

## Navigating ALMA Configuration

Access the configuration area via the **gear icon** at the bottom of the ALMA menu.

### Institution vs. Library Level

A critical distinction in ALMA configuration is the **level** at which you are working:

- **Institution level** — view and edit settings that apply to the entire institution
- **Library level** — view and edit settings for a specific library (select the library from the Configuring menu)

Always check which level is active before making changes.

### Other Settings and Customer Parameters

For each functional area at the institution level, the **General** section contains an **Other Settings** option. This is where **Customer Parameters** are found — general ALMA parameters that govern many system behaviors.

To edit a customer parameter:
1. Navigate to the relevant functional area's **Other Settings**.
2. Locate the parameter in the table.
3. Click **Row Actions → Customize**.
4. Enter a new value.
5. Click **Save**.

> Hover over a parameter's free text description to see an explanation of what it controls. Full documentation is also available in the Knowledge Center.

---

## Online Resources for ALMA Administrators

### Ex Libris System Status
Monitor whether your ALMA environment is up and running or has scheduled maintenance. Register for a personalized experience focused on your institution's servers and receive email notifications for expected downtimes.

### Ex Libris Developer Network
Technical information on ALMA's APIs, integration standards, and the ALMA Tech Blog. Available at: **developers.exlibrisgroup.com**

### Education and Knowledge Webinars
Register for live webinars presented by Ex Libris experts on a wide range of ALMA topics.

### Ex Libris YouTube Channel
Training videos, product demonstrations, and webinar recordings. Subscribe for updates.

### Ex Libris Knowledge Center
Available at: **knowledge.exlibrisgroup.com**

The ALMA section includes:

| Resource | Description |
|----------|-------------|
| **Submit a Case** | Open support tickets |
| **Knowledge Articles** | Resolved support issues and reference articles |
| **Complete ALMA Online Help** | Full product documentation |
| **Training** | ALMA training resources, including the ALMA Administration Certification |

> Successful completion of the Administration Certification exam earns you the **Certified ALMA Administrator** designation.

---

## Summary

ALMA administration is built on a clear role-based structure, with configuration organized by functional area and accessible at both institution and library levels. Understanding the distinction between read-only and full access, treating superuser roles with care, and knowing where to find documentation and support resources will serve as the foundation for everything else you do as an ALMA administrator.
