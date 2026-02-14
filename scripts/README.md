# Utility Scripts

This folder contains helper scripts for website maintenance.

## Scripts

### `make_thumbnails.sh`

**Purpose:** Generate thumbnail images for the website

**Usage:**

```bash
bash scripts/make_thumbnails.sh
```

**What it does:**

- Scans the `images/` folder for .jpg and .png files
- Creates 160x160 pixel thumbnails
- Saves thumbnails to `tn/images/` folder
- Only creates thumbnails for images that don't already have one

**Requirements:** ImageMagick (`convert` command)

Install on macOS: `brew install imagemagick`

---

### `make_favicon.sh`

**Purpose:** Generate favicon.ico from your profile image

**Usage:**

```bash
bash scripts/make_favicon.sh
```

**What it does:**

- Converts `images/circle_bw_crop.jpg` to favicon.ico
- Creates multiple sizes (16px, 24px, 32px, 48px, 64px, 72px, 96px, 128px, 256px)
- Saves to root directory as `favicon.ico`

**Requirements:** ImageMagick (`convert` command)

---

## When to Use These Scripts

**Thumbnails:** Run this when you add new project images to the `images/` folder
**Favicon:** Run this if you want to update the site icon that appears in browser tabs
