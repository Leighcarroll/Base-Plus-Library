# Base Plus Library — User Guide

This guide explains how to add and maintain projects in the Base Plus Library. Follow these instructions to keep the library consistent and useful for the whole team.

---

## What is the library?

The Base Plus Library is a shared reference tool for our team. It stores screenshots, links, and notes for every website we build — organised by project or by component type. Everything is accessible via a single link and updates in real time for everyone.

---

## Getting started

Open the library in your browser using the shared link. You will land on the main gallery showing all projects. Use the **By project** and **By type** toggle at the top to switch views.

---

## How to add a project

A project represents one client website.

1. Click **+ Add project** in the top right
2. Fill in the fields:

| Field | What to enter |
|---|---|
| Project name | The client name, e.g. `Nordvik Outdoor` |
| Website URL | The live site address, e.g. `https://nordvik.com` |
| Jira ticket URL | The full URL of the main Jira ticket for this project |
| Cover screenshot URL | A URL linking to a full-page or above-the-fold screenshot (see screenshot guide below) |

3. Click **Add project**

The project will appear as a card in the gallery immediately.

---

## How to add a component

A component is a specific section of a website — for example the header, hero banner, footer, or product grid. Each project can have multiple components.

1. Click into a project from the gallery
2. Click **+ Add component**
3. Fill in the fields:

| Field | What to enter |
|---|---|
| Component name | A clear descriptive name, e.g. `Site header` or `Full-bleed hero` |
| Component type | Choose from the dropdown list. If your component doesn't fit, choose Custom and type your own. |
| Screenshot URL | A URL linking to a cropped screenshot of just this section (see screenshot guide below) |
| GitHub code snippet URL | Direct link to the relevant file or snippet in the shared GitHub repo |
| XML / component file URL | Link to the XML file used to build this component |
| Figma URL | Link to the relevant Figma page or component |
| Notes | Any important usage instructions, warnings, or gotchas the team should know |

4. Click **Add component**

---

## How to add a mobile variant

If a component has a separate mobile version, expand the **Mobile variant** section at the bottom of the Add component form. Fill in whichever fields apply — screenshot, code link, XML file, and notes. Leave it blank if the component uses the same code on mobile.

---

## Screenshot guide

Screenshots are hosted in the GitHub repo under the `screenshots/` folder. Follow these steps to add one.

### Taking the screenshot

- Capture only the section of the page relevant to the component — not the whole page
- For headers and banners, aim for a wide crop at roughly **1600 × 400px**
- For product grids or larger sections, **1600 × 800px** works well
- Use a desktop browser at full width for desktop screenshots
- For mobile variants, use your browser's mobile preview mode (usually found in developer tools) at **390px width**
- Make sure the page is in its final published state before screenshotting — no draft content

### Naming your files

Use lowercase letters, hyphens instead of spaces, and be specific. Follow this pattern:

```
[client-name]-[component]-[variant].png
```

**Examples:**

```
nordvik-header-desktop.png
nordvik-header-mobile.png
nordvik-hero-desktop.png
marta-footer-desktop.png
greystone-mega-nav-desktop.png
greystone-mega-nav-mobile.png
```

Avoid vague names like `screenshot1.png` or `header.png` — these will clash across projects.

### Uploading to GitHub

1. Go to the shared GitHub repo
2. Click into the `screenshots/` folder (or the relevant project subfolder, e.g. `screenshots/nordvik/`)
3. Click **Add file → Upload files**
4. Drag your screenshot in and click **Commit changes**
5. Click on the uploaded image in GitHub
6. Right-click the image and select **Copy image address** — this is the URL you paste into the library

The URL will look like this:
```
https://raw.githubusercontent.com/Leighcarroll/Base-Plus-Library/main/screenshots/nordvik-header-desktop.png
```

---

## Component types

When adding a component, choose the type that best describes it. This is what powers the **By type** view, allowing the whole team to find all headers or all footers across every project at once.

The available types are:

- Header
- Navigation
- Hero
- Banner
- Product Grid
- Product Detail
- Collection
- Footer
- Sidebar
- Cart
- Checkout
- Search
- Blog
- Gallery
- Form
- Other

If you use a custom type, make sure to check with the team first so we don't end up with duplicates like `Nav` and `Navigation` for the same thing.

---

## Notes and warnings

The Notes field is important — use it to flag anything that could trip someone up when reusing or adapting this component. Good things to include:

- Breakpoint behaviour, e.g. *Collapses to single row under 768px*
- Dependencies, e.g. *Requires Klaviyo list ID to be set in theme settings*
- Things not to change, e.g. *Do not remove z-index:50 on the nav wrapper*
- External service connections, e.g. *Subscription widget is Recharge — do not modify data-recharge attributes*

---

## Editing a project or component

- To edit a **project**, open it and click **Edit** in the top right of the detail view
- To edit a **component**, click the small **Edit** button next to the component name
- Please upload and link xml files to the dnc Repo, not to this public repo

Changes save immediately to the shared storage and are visible to everyone.

---

## Things to keep in mind

- The library is shared — any change you make is live for the whole team immediately
- Screenshots must be hosted online (in the GitHub repo) before they can be linked — they cannot be uploaded directly into the library
- If a component does not have a mobile variant, leave the mobile section blank — it will show as inactive on the card
- Try to add components in the order they appear on the page, top to bottom — it makes the detail view easier to scan

