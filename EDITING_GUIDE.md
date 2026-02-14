# Quick Editing Guide

## ✏️ Most Common Edits

### Update Your Bio

```
File: _includes/bio.html
```

Edit this one file to change your bio everywhere on the site.

### Change Your Photo

```
File: images/z_me_24-06-10.jpg
```

Replace the image file (or update the filename in index.html line ~76)

### Update Social Links

```
Files: index.html (lines ~80-84)
       _layouts/default.html (lines ~48-52)
```

Edit the `<a href="...">` tags

### Add a New Project

```
Location: _posts/
Filename: YYYY-MM-DD-project-name.markdown
```

Template:

```markdown
---
layout: post
title: "Project Title"
date: 2024-01-01
image: /images/project.jpg
categories: research # or: industry, teaching, other
authors: "Your Name"
venue: "Conference/Journal"
excerpt: "Short description"
doi: "https://..." # optional
---
```

## 🚀 Publishing Changes

```bash
git add .
git commit -m "Your change description"
git push
```

Wait 2-3 minutes → Hard refresh browser (`Cmd + Shift + R`)

## 📁 File Structure Quick Reference

| What to Edit    | File                       |
| --------------- | -------------------------- |
| Bio text        | `_includes/bio.html`       |
| Site name       | `_config.yml`              |
| Homepage layout | `index.html`               |
| Post layout     | `_layouts/default.html`    |
| Projects        | `_posts/*.markdown`        |
| Photo           | `images/z_me_24-06-10.jpg` |
| Styles          | `style.scss`               |

## ❗ Important Notes

- Always include front matter (`---` at top of files) in .html files for Jekyll to process them
- Images go in `images/` folder, thumbnails in `tn/images/`
- Changes take 2-3 minutes to deploy to live site
- Hard refresh browser to see changes (clears cache)

## 📖 Full Documentation

See [README.md](README.md) for complete documentation and troubleshooting.
