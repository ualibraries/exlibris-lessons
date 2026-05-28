# Alma Analytics: Configuring and Reporting on User Statistics

## Overview

Alma's analytics engine includes standard user attributes such as birthdate, full name, job category, and user group. Beyond these, Alma provides **five configurable user statistics slots** (called Statistical Categories) that you can map to custom data of your choosing.

**Examples of custom statistical categories:**
- Academic discipline
- Country of origin
- Dietary preference

This tutorial walks through the full setup process and shows how to use these statistics in a report.

---

## Configuration Workflow at a Glance

1. Create a **Category Type** (e.g., *Dietary Preference*)
2. Define **Statistical Categories** — the possible values (e.g., *Vegan*, *Vegetarian*, *Omnivore*)
3. **Map** the statistical categories to their category type
4. **Assign** the category type to one of the five Analytics User Statistics slots
5. **Attribute** a statistical category to individual users
6. **Create a report** using the configured user statistics

---

## Step 1: Create a Category Type

Navigate to: **Alma Configuration > User Management > User Details > Category Types**

The code table displays existing category types (e.g., Discipline, Country of Origin).

> **Note:** You can create as many category types as you want, but only five will be available in Analytics.

To create a new type:

1. Click **Add Row**
2. Enter a unique **Code** and a **Description** (e.g., Code: `DIET_PREF`, Description: `Dietary Preference`)
3. Optionally set this as the **default type** (used when loading users via API) — not required for most cases
4. Click **Add Row** to confirm
5. Click **Save**

---

## Step 2: Define Statistical Categories (Possible Values)

Navigate to: **Configuration > User Management > User Details > Statistical Categories**

The code table shows all existing statistical categories. For example, *Social Sciences* and *Psychology* are possible values under the *Discipline* category type.

To add new values for Dietary Preference:

1. Click **Add Row** for each value you want to create:
   - Omnivore
   - Vegetarian
   - Vegan
2. Follow the same process used to add category types
3. Click **Save**

---

## Step 3: Map Statistical Categories to a Category Type

Navigate to: **Configuration > User Management > User Details > Statistical Categories Types**

The mapping table shows which statistical categories belong to which category type (e.g., *Australia* is mapped to *Country of Origin*).

To map your new values:

1. Click **Add Row**
2. Select the **Statistical Category** (e.g., Vegan)
3. Select the **Category Type** (e.g., Dietary Preference)
4. Click **Add Row**
5. Repeat for each remaining value (Vegetarian, Omnivore)
6. Click **Save**

---

## Step 4: Assign the Category Type to an Analytics User Statistics Slot

Navigate to: **Configuration > Analytics > General Configuration > Analytics User Statistics**

The code table shows how each of the five **Analytics User Statistics** slots (Statistics 1–5) maps to a category type.

To assign your new category type:

1. Locate **Statistics 5** (or whichever slot is available)
2. Enable it and map it to **Dietary Preference**
3. Click **Save**

Configuration is now complete.

---

## Step 5: Assign a Statistical Category to a User

1. In Alma, search for a user (e.g., *John Abraham*)
2. Click on their name to open the edit view
3. Go to the **Statistics** tab
   - Existing statistics are shown (e.g., John has *Chemistry* under *Discipline*)
4. Click **Add Statistic**
5. Select the **Category Type**: Dietary Preference
6. Select the **Statistical Category**: Vegan
7. Click **Add and Close**
8. Click **Save**

> **Alternative methods:** User statistics can also be assigned via the **Users integration** or through **Alma's APIs** for bulk updates.

---

## Step 6: Create a User Statistics Report in Analytics

1. Navigate to **Analytics > Design Analytics**
2. Click **Create > Analysis**
3. Choose the subject area: **Users**

### Select Report Columns

Under **User Details**, add:

- **Full Name** (or other desired attributes)
- **Statistical Category 5** — this corresponds to Dietary Preference

### Add a Filter

To exclude users with no value in this field:

1. Click the gear icon next to **Statistical Category 5**
2. Choose **Filter**
3. Set the condition to **is not null**
4. Click **OK**

### View Results

Click the **Results** tab. The report displays each user by name with their Dietary Preference shown in the Statistical Category 5 column.

---

## Summary

| Step | Location in Alma |
|---|---|
| Create Category Type | Configuration > User Management > User Details > Category Types |
| Define Statistical Categories | Configuration > User Management > User Details > Statistical Categories |
| Map Categories to Type | Configuration > User Management > User Details > Statistical Categories Types |
| Assign to Analytics Slot | Configuration > Analytics > General Configuration > Analytics User Statistics |
| Assign to a User | User record > Statistics tab |
| Report on User Statistics | Analytics > Design Analytics > Create Analysis > Users subject area |

> **Reminder:** Only five category types can be active in Analytics at one time, so plan your slot usage carefully across your institution.
