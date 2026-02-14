# Personal Website - martinspacheco.github.io

My personal academic website showcasing research, industry, teaching, and private projects.

## 🚀 Quick Start - Making Changes

### 1. Update Your Bio
**File:** `_includes/bio.html`

This single file controls your bio text across the entire website. Edit it and push to update everywhere.

### 2. Update Your Photo
**File:** `images/z_me_24-06-10.jpg`

Replace this file with your photo (keep the same filename, or update the filename in `index.html` line ~76 and `_layouts/default.html` line ~45)

### 3. Update Your Name
**File:** `index.html` (line ~48) and `_layouts/default.html` (line ~33)

Change the text inside `<h1>Your Name</h1>`

### 4. Update Social Links
**File:** `index.html` (lines ~80-84) and `_layouts/default.html` (lines ~48-52)

Edit the `<a href="">` links

### 5. Add a New Project
**Location:** `_posts/` folder

Create a new file named `YYYY-MM-DD-project-name.markdown` with this template:

```markdown
---
layout: post
title: "Your Project Title"
date: 2024-01-01
image: /images/project-image.jpg
categories: research  # Options: research, industry, teaching, or other
authors: "Your Name, Collaborator Name"
venue: "Conference or Journal Name"
excerpt: "Short description of your project that appears on the homepage."
doi: "https://doi.org/..."  # optional
video: "https://..."  # optional
website: "https://..."  # optional
---
```

## 📁 Repository Structure

```
├── index.html              # Main homepage
├── _config.yml             # Site configuration (name, URL, settings)
├── style.scss              # Main stylesheet
│
├── _includes/
│   └── bio.html           # Your bio text (edit this!)
│
├── _layouts/
│   ├── default.html       # Layout for post pages
│   └── post.html          # Simple wrapper for posts
│
├── _posts/                # All your projects go here
│   ├── 2024-01-01-project1.markdown
│   └── 2024-02-01-project2.markdown
│
├── _sass/                 # stylesheet components
│   ├── _highlights.scss
│   ├── _reset.scss
│   ├── _svg-icons.scss
│   └── _variables.scss
│
├── images/                # Full-size images
├── tn/images/            # Thumbnails (auto-generated)
└── pdfs/                  # PDF files (papers, posters, etc.)
```

## 🔧 How It Works

1. **Jekyll** processes the files and generates a static website
2. **GitHub Pages** hosts the site automatically from this repository
3. Changes pushed to `main` branch are live within 2-3 minutes

### Important Files Explained

| File | Purpose | When to Edit |
|------|---------|--------------|
| `_includes/bio.html` | Your biography | Update your bio |
| `index.html` | Homepage structure | Change layout/sections |
| `_layouts/default.html` | Individual post pages | Change post layout |
| `_config.yml` | Site settings | Change site name/URL |
| `_posts/*.markdown` | Project entries | Add new projects |

## 📝 Publishing Changes

```bash
# 1. Make your changes to files
# 2. Check what changed
git status

# 3. Stage all changes
git add .

# 4. Commit with a message
git commit -m "Describe your changes"

# 5. Push to GitHub
git push

# 6. Wait 2-3 minutes, then hard refresh your browser (Cmd + Shift + R)
```

## 🎨 Customization

### Change Colors/Fonts
Edit `style.scss` and files in `_sass/` folder

### Change Google Analytics ID
Edit `index.html` line ~16 and `_layouts/default.html` line ~7

### Remove Sections
In `index.html`, delete or comment out entire `<div>` blocks for:
- Research Projects
- Industry Projects  
- Teaching Projects
- Private Projects

## 🛠️ Technical Details

- **Built with:** Jekyll (static site generator)
- **Hosted on:** GitHub Pages
- **Domain:** www.martinspacheco.de (configured via CNAME file)
- **Design:** Based on Jon Barron's academic website template

## ❓ Troubleshooting

**Q: Changes not showing up?**
- Wait 2-3 minutes for GitHub Pages to rebuild
- Hard refresh your browser: `Cmd + Shift + R` (Mac) or `Ctrl + Shift + R` (Windows)
- Check if changes were pushed: `git log --oneline -3`

**Q: Images not displaying?**
- Images must be in `images/` folder
- Thumbnails must be in `tn/images/` folder (or update paths in `index.html`)
- Check file names match exactly (case-sensitive)

**Q: Jekyll template variables not working ({{ site.name }} shows literally)?**
- Make sure files have front matter at the top (--- ---)
- Check `_config.yml` has the right variable names

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## 📄 License

Design and source code adapted from [Jon Barron's website](https://jonbarron.info) modified by [Leonid Keselman](https://leonidk.com)
