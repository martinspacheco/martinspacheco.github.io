# Personal Website - martinspacheco.github.io

My personal academic website showcasing research, industry, teaching, and private projects.

---

## ⚡ Quick Reference

| What to Edit | File                        | Action                            |
| ------------ | --------------------------- | --------------------------------- |
| Bio text     | `_includes/bio.html`        | Edit and push                     |
| Your photo   | `images/z_me_24-06-10.jpg`  | Replace file                      |
| Your name    | `index.html` (line ~48)     | Change `<h1>` text                |
| Social links | `index.html` (lines ~80-84) | Edit `<a href>` tags              |
| Add project  | `_posts/`                   | Create `YYYY-MM-DD-name.markdown` |
| Colors/fonts | `_sass/_variables.scss`     | Edit variables                    |

### 🚀 Publishing Changes

```bash
git add .
git commit -m "Describe your changes"
git push
```

Wait 2-3 minutes → Hard refresh browser: `Cmd + Shift + R` (Mac) or `Ctrl + Shift + R` (Windows)

---

## � How To

### Update Bio

Edit `_includes/bio.html` - changes apply everywhere automatically

### Add New Project

Create `_posts/YYYY-MM-DD-project-name.markdown` with this template:

```markdown
---
layout: post
title: "Your Project Title"
date: 2024-01-01
image: /images/project-image.jpg
categories: research # or: industry, teaching, other
authors: "Your Name"
venue: "Conference/Journal"
excerpt: "Short description"
doi: "https://..." # optional
video: "https://..." # optional
---
```

After adding images, run: `bash scripts/make_thumbnails.sh`

### Change Colors/Fonts

Edit `_sass/_variables.scss`

### Update Google Analytics

Edit `index.html` and `_layouts/default.html` (search for "gtag")

---

## 📁 Repository Structure

### What File Should I Edit?

| What You Want to Change    | Edit This File                    | Location     |
| -------------------------- | --------------------------------- | ------------ |
| Biography text             | `bio.html`                        | `_includes/` |
| Add new project            | Create `YYYY-MM-DD-name.markdown` | `_posts/`    |
| Change colors              | `_variables.scss`                 | `_sass/`     |
| Change homepage layout     | `index.html`                      | root         |
| Change project page layout | `default.html`                    | `_layouts/`  |
| Site name/URL              | `_config.yml`                     | root         |

### Complete Structure

```
martinspacheco.github.io/
│
├── 🏠 FRONTEND (What visitors see)
│   ├── index.html              # Homepage with bio & project grid
│   └── style.scss              # Main stylesheet (compiles SASS)
│
├── 🎨 STYLING (Colors, fonts, design)
│   └── _sass/                  # Modular stylesheets
│       ├── _variables.scss     # Colors, fonts, sizes ⬅ Edit colors here
│       ├── _reset.scss         # Browser normalization
│       ├── _highlights.scss    # Code block styling
│       └── _svg-icons.scss     # Social media icon styles
│       └── 📖 README.md
│
├── 📄 CONTENT (Your projects & bio)
│   ├── _posts/                 # Project posts ⬅ Add projects here
│   │   ├── 2024-06-01-steam.markdown
│   │   ├── 2024-04-01-tms-tum.markdown
│   │   ├── ... (24 total)
│   │   └── 📖 README.md
│   │
│   ├── _includes/              # Reusable content blocks
│   │   ├── bio.html            # Biography ⬅ Edit bio here
│   │   └── 📖 README.md
│   │
│   ├── images/                 # Full-size images (50+ files)
│   ├── tn/images/             # Thumbnails (auto-generated)
│   └── pdfs/                   # Downloadable PDFs
│
├── 🏗️ STRUCTURE (Templates & config)
│   ├── _layouts/               # Page templates
│   │   ├── default.html        # Main wrapper (header, footer, nav)
│   │   ├── post.html           # Project post template
│   │   └── 📖 README.md
│   │
│   └── _config.yml             # Jekyll configuration
│
├── 🔧 TOOLS (Utilities)
│   └── scripts/                # Helper scripts
│       ├── make_thumbnails.sh  # Generate image thumbnails
│       ├── make_favicon.sh     # Create site favicon
│       └── 📖 README.md
│
├── ⚙️ CONFIGURATION
│   ├── _config.yml             # Site settings, plugins, excludes
│   ├── .gitignore             # Ignored files
│   ├── CNAME                  # Custom domain (martinspacheco.de)
│   └── LICENSE                # MIT License
│
└── 📖 DOCUMENTATION
    └── README.md               # This comprehensive guide
```

**💡 Tip:** Each major folder (`_includes/`, `_layouts/`, `_posts/`, `_sass/`, `scripts/`) has its own README with detailed information.

## 🔧 How It Works

1. **Jekyll** processes the files and generates a static website
2. **GitHub Pages** hosts the site automatically from this repository
3. Changes pushed to `main` branch are live within 2-3 minutes

### Important Files Explained

| File                    | Purpose               | When to Edit           |
| ----------------------- | --------------------- | ---------------------- |
| `_includes/bio.html`    | Your biography        | Update your bio        |
| `index.html`            | Homepage structure    | Change layout/sections |
| `_layouts/default.html` | Individual post pages | Change post layout     |
| `_config.yml`           | Site settings         | Change site name/URL   |
| `_posts/*.markdown`     | Project entries       | Add new projects       |

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

---

## ❗ Important Notes

- **Front Matter Required:** HTML files need `---` at the top for Jekyll to process template variables
- **Image Locations:** Full-size images → `images/`, thumbnails → `tn/images/`
- **Deploy Time:** Changes take 2-3 minutes to appear on live site
- **Cache Clearing:** Always hard refresh (`Cmd/Ctrl + Shift + R`) to see updates
- **Case Sensitive:** File and folder names are case-sensitive on the server
- **File Naming:** Posts must be named `YYYY-MM-DD-title.markdown`

---

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

**Q: Need more help?**

- Check comments in the actual file you're editing (all code is extensively commented)
- Read the specific folder's README for detailed information
- Review Jekyll documentation for template syntax

---

## ✅ Best Practices

1. **One change at a time** - Easier to debug if something breaks
2. **Descriptive commit messages** - "Update bio" is better than "changes"
3. **Read folder READMEs** - Each major folder has specific guidance
4. **Hard refresh browser** - Always use `Cmd+Shift+R` / `Ctrl+Shift+R` to clear cache
5. **Test locally** - Run `jekyll serve` to preview before pushing (optional)
6. **Back up images** - Keep originals before running thumbnail scripts

---

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)

## 📄 License

Design and source code adapted from [Jon Barron's website](https://jonbarron.info) modified by [Leonid Keselman](https://leonidk.com)
