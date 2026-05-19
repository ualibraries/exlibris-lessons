# ALMA Analytics User Statistics: Configuration Tutorial

## Overview

When generating Analytics reports on your users, ALMA provides standard attributes such as birthdate, full name, job category, and user group. In addition, ALMA offers **five generic user attributes** called **Statistical Categories**, which you can configure for any custom data your institution needs.

**Examples of custom statistical categories:**
- Academic discipline
- Country of origin
- Dietary preference

In this tutorial, you will learn how to:
1. Create category types (e.g., *Country of Origin*)
2. Define statistical categories — the possible values within a type (e.g., *Germany*, *Canada*)
3. Map statistical categories to their category types
4. Assign a category type to one of the five Analytics User Statistics slots
5. Attribute a statistical category to an individual user
6. Create an Analytics report using user statistics

---

## Step 1: Create a Category Type

Navigate to:

**ALMA Configuration → User Management → User Details → Category Types**

The code table displays your existing category types (e.g., *Discipline*, *Country of Origin*).

> **Note:** You can create as many category types as you want, but only **five** will be available in Analytics at any time.

To add a new category type:
1. Click **Add Row**.
2. Enter a unique **Code** and a **Description** (e.g., Code: `DIET_PREF`, Description: `Dietary Preference`).
3. Optionally, check **Default Type** — this will pre-select this type when loading users via API.
4. Click **Add Row** to confirm.
5. Click **Save**.

---

## Step 2: Define Statistical Categories (Possible Values)

Navigate to:

**ALMA Configuration → User Management → User Details → Statistical Categories**

The code table displays all existing statistical categories (e.g., *Social Sciences* and *Psychology* are possible values for the *Discipline* type).

To add new statistical categories (e.g., for dietary preference):
1. Click **Add Row**.
2. Enter a **Code** and **Description** for each value (e.g., *Omnivore*, *Vegetarian*, *Vegan*).
3. Repeat for each value you need.
4. Click **Save**.

---

## Step 3: Map Statistical Categories to a Category Type

Navigate to:

**ALMA Configuration → User Management → User Details → Statistical Categories → Types**

The mapping table shows how statistical categories are associated with their category type (e.g., *Australia* is a possible value for *Country of Origin*).

To map your new categories to their type:
1. Click **Add Row**.
2. Select the **Statistical Category** (e.g., *Omnivore*).
3. Assign it to the **Category Type** (e.g., *Dietary Preference*).
4. Click **Add Row** to confirm.
5. Repeat for each remaining category value.
6. Click **Save**.

---

## Step 4: Assign a Category Type to an Analytics User Statistics Slot

ALMA provides five Analytics User Statistics slots, each of which can be mapped to one category type.

Navigate to:

**ALMA Configuration → Analytics → General Configuration → Analytics User Statistics**

The code table shows the current mapping of each of the five statistics slots to a category type.

To assign your new category type:
1. Locate an unused statistics slot (e.g., *Statistics 5*).
2. Enable it and map it to your category type (e.g., *Dietary Preference*).
3. Click **Save**.

Your configuration is now complete. Statistical Category 5 = Dietary Preference.

---

## Step 5: Assign a Statistical Category to a User

To attribute a statistical category to an individual user:

1. In ALMA, search for the user (e.g., *John Abraham*) and click their name to open the user record.
2. Go to the **Statistics** tab.
   - You can see any existing statistical categories already assigned (e.g., *Chemistry* for the *Discipline* type).
3. Click **Add Statistic**.
4. Select the **Category Type** (e.g., *Dietary Preference*) and the **Statistical Category** (e.g., *Vegan*).
5. Click **Add and Close**.
6. Click **Save** to save the user record.

> **Tip:** User statistics can also be added in bulk via the **Users integration** or **ALMA APIs**.

---

## Step 6: Create an Analytics Report Using User Statistics

Navigate to:

**ALMA → Analytics → Design Analytics**

1. Click **Create → Analysis**.
2. For the **Subject Area**, select **Users**.
3. Under **User Details**, select the attributes you want to include:
   - *Full Name* (or other standard user attributes)
   - *Statistical Category 5* (your newly configured Dietary Preference field)
4. Add a **filter** on Statistical Category 5:
   - Set the condition so the field **is not null** — this ensures only users with a Dietary Preference assigned appear in the report.
5. Click **OK**.
6. Open the **Results** tab to view the report.

The report will display users listed by name with their Dietary Preference value shown in the Statistical Category 5 column.

---

## Summary

User statistical categories give your institution a flexible way to capture and report on custom user data beyond ALMA's standard attributes. By configuring category types, defining values, mapping them to the five Analytics slots, and assigning them to users, you can generate tailored user reports that reflect the specific demographics or characteristics your institution needs to track.

| Configuration Step | Navigation Path |
|---|---|
| Create Category Types | Configuration → User Management → User Details → Category Types |
| Define Statistical Categories | Configuration → User Management → User Details → Statistical Categories |
| Map Categories to Types | Configuration → User Management → User Details → Statistical Categories → Types |
| Assign to Analytics Slot | Configuration → Analytics → General Configuration → Analytics User Statistics |
| Assign to a User | User Record → Statistics tab |
| Create Report | Analytics → Design Analytics → Create → Analysis → Users |
