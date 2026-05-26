# Primo VE UI Customization: A Tutorial

## Overview

Primo VE allows you to customize the look and feel of the patron-facing interface, including colors, logos, images, and other branding elements. There are two methods for customization:

1. **Customization Package** — download, edit, and upload a package of CSS, HTML, JavaScript, and image files
2. **Primo Studio** — a visual, point-and-click customization tool

> **Important:** UI customization is the **institution's responsibility**, not Ex Libris. Contact support if you have questions.
>
> It is strongly recommended that you use **only one** of these two methods to avoid conflicts and errors.

---

## Method 1: The Customization Package

The Customization Package gives you full control over the interface by editing source files directly. If no package is uploaded, the system uses out-of-the-box configurations.

### Accessing the Package

Navigate to:

**ALMA Configuration → Discovery → Display Configuration → Configure Views**

Open the Row Action tool for the view you want to customize and select **Edit**. Then click the **Manage Customization Package** tab.

### Downloading a Package

Three package types are available:

| Package | When to Use |
|---------|-------------|
| **Current View Customization Package** | When your view has already been customized — download to get the latest version |
| **Template View Customization Package** | When customizing for the first time (if Current View Package is greyed out) |
| **Central Customization Package** | For consortium administrators to define a shared package for member institutions (requires Discovery Administrator role for the Network Zone) |

Click **Download** to begin. The package downloads as a **.zip file**.

### Package Structure

When unzipped, the top folder should be titled with your **View Code** and contain four subfolders:

```
InstitutionCode-ViewCode/
├── CSS/
├── HTML/
├── IMG/
└── JS/
```

> You should be familiar with **CSS**, **HTML**, **JavaScript**, and **AngularJS** to work with these files. For guidance on customizing specific files, see the Knowledge Center.

### Uploading a Customized Package

1. Make your edits to the unzipped files.
2. Re-zip the folder.
   > Use **7-Zip** or **WinRAR** rather than Windows "Send to → Compressed Folder" to avoid upload errors.
3. Ensure the top folder of the zip file follows the format: `InstitutionCode-ViewCode`
4. On the Manage Customization Package tab, click the **folder icon** in the Upload Package section.
5. Locate the zip file and click **Upload**.

### Adding a Clickable Logo

On the same tab, you can upload a **logo file** and enter the **URL** it should link to when clicked (typically the main Discovery page).

---

## Method 2: Primo Studio

Primo Studio is a visual customization tool that lets you preview and adjust your interface without editing code directly.

### Accessing Primo Studio

From the View Configuration page (**Configure Views → Edit**), click the **Primo Studio** link. Primo Studio loads with the default customization package.

### What You Can Customize in Primo Studio

Using the options along the left side of the interface:
- **Colors** — adjust the color scheme
- **Images** — upload a logo, favicon, and resource type images
- **Add-ons** — enable community-created and community-shared add-ons

Changes are **immediately reflected in the preview** on the right side of the screen.

> For details on each customization section in Primo Studio, see the Knowledge Center.

### Saving Your Work

> **Critical:** If you do not download your package after making changes in Primo Studio, **all modifications will be lost**.

After making changes:
1. Click the **Download Package** tab.
2. Save the package to your local machine.

This saved package can be:
- Reloaded into Primo Studio later for further editing
- Deployed to your live interface via ALMA Configuration

### Resuming Work on a Saved Package

1. In Primo Studio, click the **Upload Package** tab.
2. Click **Choose Package** and locate your saved file.
3. Click **Upload Package** — Primo Studio will load the file and display it in the preview.

### Deploying to Production

Once satisfied with your changes:
1. Download the package from Primo Studio.
2. Return to **ALMA Configuration → Configure Views → Manage Customization Package**.
3. Upload the downloaded package using the standard upload process.

---

## Summary

Both the Customization Package and Primo Studio provide paths to a branded, institution-specific Primo VE interface. The Customization Package offers the most control for institutions comfortable with front-end web development, while Primo Studio provides a more accessible visual workflow. Whichever method you choose, use it consistently — mixing the two methods is not recommended.
