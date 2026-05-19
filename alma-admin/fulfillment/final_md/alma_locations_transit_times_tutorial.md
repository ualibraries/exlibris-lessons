# ALMA Locations and Transit Time Rules: A Configuration Tutorial

## Overview

ALMA's organizational structure is a hierarchy: **Institution → Libraries → Locations**. Physical item locations are associated with a specific library and are the foundation for how items circulate. The **fulfillment unit** attached to a location is the first step in determining loan attributes for items shelved there.

In this tutorial, you will learn how to:
- Create and configure physical locations
- Attach a circulation desk to a location
- Configure transit time rules for moving items between libraries

---

## Accessing Physical Locations

Physical locations are configured at the **library level**, not the institution level.

1. Select your **library** from the Configuring menu.
2. Navigate to either:
   - **Fulfillment → Locations → Physical Locations**, or
   - **General → Locations → Physical Locations**

The page displays all current locations at your library, including code, name, type, and associated fulfillment unit. Use the drop-downs to filter by location type or fulfillment unit.

### Managing Existing Locations

From the **Row Action** tool, you can:
- **Edit** — modify a location *(note: changes may affect multiple functional areas in ALMA; coordinate carefully)*
- **Duplicate** — copy an existing location as a starting point
- **Delete** — remove a location *(the location must have no inventory associated with it; all items must be moved first)*

---

## Creating a New Location

1. Click **Add Location**.
2. Fill in the required fields:
   - **Code** — unique identifier
   - **Name** — display name
   - **Type** — determines patron access:

| Type | Description |
|------|-------------|
| **Open** | Accessible to patrons |
| **Closed Stacks** | Staff retrieval only |
| **Remote Storage** | Off-site storage |
| **Not in Library** | Items not physically in the library (e.g., instructor copies) |

3. Fill in any additional fields as needed.
4. Click **Add Location**.

---

## Attaching a Circulation Desk to a Location

Attaching a circulation desk enables handling times for workflows such as picking from shelf, checking in/out, and reshelving.

1. Open the **Row Action** tool for the new location and select **Edit**.
2. Scroll to the **Physical Location Circulation Desk's List** section.
3. Choose one of two options:
   - **Add New Circulation Desk** — launches a wizard to create a new desk and attach it

     > For details on creating a circulation desk, see the Circulation Desk session in the Alma Essentials Training in the Knowledge Center.

   - **Attach Existing Circulation Desk** — select a desk from the drop-down
4. Choose which **services** this desk will perform for this location.

   > You can attach more than one circulation desk if a single desk does not cover all services.

5. Click **Attach Existing Circulation Desk** (or complete the new desk wizard).
6. Click **Save**.

---

## Configuring Transit Time Rules

Transit time rules tell ALMA how long it takes to transfer a physical item from one library to another. This allows ALMA to calculate the feasibility and estimated delivery time for fulfillment requests.

Transit time rules are configured at the **institution level**.

### Accessing Transit Time Rules

1. Switch the Configuring menu to the **institution level**.
2. Navigate to: **Fulfillment → Library Management → Transit Time**

### Estimating Transit Time (Optional)

Before adding a rule, you can test the current configuration:
1. Click **Calculate ETA**.
2. Enter the **from** library, **to** library, material type, location, and start time.
3. Click **Calculate ETA** to see the estimated delivery time.
4. Click the **back arrow** when done.

### Creating a New Transit Time Rule

1. Click **Add Rule**.
2. Enter a **Name** (required) and **Delivery Time in hours** (required).
3. Configure the scope:
   - **From** — source library (supports multiple selections; selecting a specific item location limits you to one)
   - **To** — destination library
   - **Start Time** — enter `*` to calculate for any start time
4. Click **Save**.

> **Example:** A rule from the Music Library to the Main Library General Location with a delivery time of 6 hours means ALMA will estimate 6 hours for any item transferred on that route.

---

## Summary

Properly configured locations and transit time rules ensure that ALMA accurately reflects your physical environment — from where items are shelved to how long it takes to move them between buildings. Always attach new locations to a circulation desk and configure transit times whenever items routinely move between libraries.
