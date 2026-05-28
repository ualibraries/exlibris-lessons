# Primo VE User Interface Customization: A Tutorial

## Overview

Primo VE ships with a default template, but you are encouraged to customize the user interface to match your institutional branding. This tutorial covers the practical steps for making the most common customizations, including:

- Logo and its clickable link
- Favicon and browser tab title
- Theme color
- Homepage banner image and text
- Homepage HTML content

Some customizations are made **within ALMA** and take effect immediately. Others require downloading, editing, and re-uploading the **Customization Package**.

> **Note:** UI customization is the **institution's responsibility**, not Ex Libris. Contact support if you have questions.

---

## Step 1: Download the Customization Package

Navigate to:

**ALMA → Discovery → Display Configuration → Configure Views**

1. **Copy the view code** of the view you want to customize — you will need it shortly.
2. Open the Row Action tool for that view and select **Edit**.
3. Click the **Manage Customization Package** tab.

### Choosing Which Package to Download

| Package | When to Use |
|---------|-------------|
| **Template View Customization Package** | First-time customization (default, out-of-the-box) |
| **Current View Customization Package** | You have already customized this view and want to build on existing changes |
| **Central Customization Package** | Consortium with unified branding; requires Discovery Administrator role for the Network Zone |

Click **Download** for the appropriate package. It downloads as a **.zip file**.

---

## Step 2: Prepare the Package Folder

1. Locate and extract the downloaded zip file.
2. Inside, find the folder called **View Code**.
3. **Rename this folder** to match your view code (copied in Step 1).
   - The colon (`:`) in the view code is not a valid folder character — **replace it with a hyphen** (e.g., `InstitutionName-ViewName`).

### Package Folder Structure

```
InstitutionName-ViewName/
└── Assets/
    ├── CSS/
    ├── HTML/
    ├── IMG/ (Images/)
    │   └── Icons/
    └── JS/
```

---

## Step 3: Make Your Customizations

### Replace the Logo

1. Open the **Assets → Images** folder.
2. Replace the default logo with your PNG file, **keeping the same filename**: `library-logo`.

### Replace the Favicon

1. Open the **Assets → Images → Icons** folder.
2. Add your favicon file, named exactly: `favicon.ico`

> Use an online tool to convert your image to `.ico` format if needed.

### Replace the Homepage Background Image

1. Open the **Assets → Homepage** folder.
2. Add an SVG file named exactly: `homepage_background.svg`

### Customize the Homepage HTML

The **Homepage** folder also contains a template file for the entire homepage in HTML format.

1. **Make a copy** of the template file.
2. **Remove the `.tmpl` suffix** from the copy's filename.
3. Open the copy with an HTML editor and make your changes.
   - Example: Change a section label from *FAQ* to *Help*
   - You can delete entire sections that do not serve your audience
4. Save your changes.

#### Multi-Language Homepages

For institutions with multiple UI languages, create a **separate homepage file for each language**, using the relevant language code in the filename. Patrons can then select which language version to display.

### CSS and JavaScript Customization

For institutions with front-end development experience, further customizations can be made in the **CSS** and **JS** folders within the package.

---

## Step 4: Upload the Customized Package

1. **Zip** the renamed folder back up.

   > Use **7-Zip** or **WinRAR** rather than Windows "Send to → Compressed Folder" to avoid upload errors. Ensure the top-level folder of the zip is the renamed View Code folder.

2. Return to ALMA: **Configure Views → Edit → Manage Customization Package tab**.
3. In the **Upload Package** section, click the **folder icon**, locate your zip file, and click **Open**.
4. Click **Upload**.
5. Click **Save** to apply your changes.

---

## Step 5: Additional Customizations Within ALMA

Some elements can be customized directly in ALMA without editing the package:

### Color Theme

From the **Manage Customization Package** tab, select a **color theme**. The chosen theme affects many visual elements while adhering to accessibility guidelines for color and contrast.

### Logo Clickable URL

1. Go to the **General** tab of the view editor.
2. In the **Logo Clickable URL** field, enter the webpage address the logo should link to (e.g., the main Discovery page).
3. Click **Save**.

### Browser Tab Title

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Labels**

1. Find the **Header Footer Tiles** table.
2. Click the Row Action button → **Customize**.
3. Locate the **main title** code and customize its description.
4. Click **Customize** to save.

### Homepage Banner Text

The large text on the landing page banner is controlled by the label code `nde.landing.header`.

1. Search for this code in the Labels page to find its table.
2. Click the Row Action button → **Customize**.
3. Search for the code within the table.
4. To create a **view-specific** banner (different text per view):
   - Click **Add Row**
   - Enter the view name, followed by a dot, then the label code (e.g., `ViewName.nde.landing.header`)
   - Enter the desired banner text in the Description field
   - Click **Add Row**
5. Click **Customize** to save.

---

## Result

After uploading and saving, your customized view will display:
- New logo and favicon
- Updated browser tab title
- New theme color
- Customized homepage banner text and layout

---

## Advanced Customization

Further options include:
- Generating a custom color theme
- Developing custom components
- Integrating third-party systems via add-on configuration in ALMA

> For more information, see the Knowledge Center and the Primo Developer Network.

---

## Summary

Primo VE UI customization is a layered process. Start with the Customization Package to replace images and edit HTML, upload it back to ALMA, and then use ALMA's built-in tools to set colors, logo links, and key labels. Always use 7-Zip or WinRAR when re-zipping your package, and always rename the top-level folder to match your view code before uploading.
