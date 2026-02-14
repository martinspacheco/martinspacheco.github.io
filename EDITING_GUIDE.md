# How to Update Your Website

## Quick Reference

### Update Your Bio

**File:** `_includes/bio.html`

Edit this single file to update your bio across the entire website. No need to edit multiple files!

### Update Other Content

- **Homepage structure:** `index.html`
- **Post layout:** `_layouts/default.html`
- **Individual posts:** `_posts/` folder

## Publishing Changes

After making edits:

```bash
git add .
git commit -m "Your change description"
git push
```

Wait 2-3 minutes for GitHub Pages to rebuild, then hard refresh your browser (`Cmd + Shift + R`).

## Structure Overview

```
_includes/
  bio.html           ← Your bio (used everywhere)
_layouts/
  default.html       ← Layout for posts
  post.html          ← Post template
index.html           ← Homepage (includes bio.html)
_posts/               ← Blog posts
```

## Troubleshooting

**Changes not showing?**

1. Verify changes are pushed: `git status`
2. Check GitHub Actions build status
3. Hard refresh browser: `Cmd + Shift + R`
4. Clear browser cache completely
