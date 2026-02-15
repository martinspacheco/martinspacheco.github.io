# Posts Folder

This folder contains all your project entries that appear on the website.

## How It Works

Each `.markdown` file in this folder becomes a project displayed on your website. Projects are automatically organized into sections based on their `categories` field.

## File Naming Convention

Files must be named: `YYYY-MM-DD-project-name.markdown`

**Example:** `2024-01-15-my-research-project.markdown`

The date determines the order projects appear (newest first).

## Project Template

```markdown
---
layout: post
title: "Your Project Title"
date: 2024-01-15
image: /images/project-image.jpg
categories: projects # Options: projects, teaching, private, publications-talks-patents
authors: "Your Name, Collaborator Names"
venue: "Conference Name or Journal"
excerpt: "Short description that appears on the homepage (1-2 sentences)"

# Optional fields:
doi: "https://doi.org/10.xxxx/xxxxx"
video: "https://youtube.com/..."
video2: "https://..." # For a second video
code: "https://github.com/..."
poster: "/pdfs/poster.pdf"
slides: "/pdfs/slides.pdf"
fullpaper: "/pdfs/paper.pdf"
website: "https://project-website.com"
website2: "https://..." # For a second website
youtube: "https://youtube.com/..."
---
```

## Categories

Projects are automatically sorted into sections:

- **`research`** → Research Projects section
- **`industry`** → Industry Projects section
- **`teaching`** → Teaching Projects section
- **`other`** (or any other value) → Private Projects section

## Adding a New Project

1. Create a new file: `2024-XX-XX-project-name.markdown`
2. Copy the template above
3. Fill in your project details
4. Add your project image to `/images/` folder
5. Generate thumbnail: `bash scripts/make_thumbnails.sh`
6. Commit and push

## Tips

- **Images:** Full-size images go in `/images/`, thumbnails in `/tn/images/`
- **PDFs:** Upload papers/posters to `/pdfs/` folder
- **Dates:** Use the actual project/publication date for accurate chronological ordering
- **Excerpts:** Keep short and engaging (appears on homepage)
- **Links:** All optional fields can be omitted if not applicable
