# Layouts Folder

This folder contains page templates that define the structure and layout of your website pages.

## How Layouts Work

Layouts are like wrappers around your content. They provide the common HTML structure (header, navigation, footer) so you don't have to repeat it in every page.

## Current Layouts

### `default.html`

**Purpose:** Main layout for the entire website

**Used by:** Project pages (via `post.html`)

**Contains:**

- Full page HTML structure
- Bio section with photo
- All project sections (Research, Industry, Teaching, Private)
- Social links
- Footer

**Note:** Due to `permalink: /` in `_config.yml`, this layout currently displays the same content as the homepage.

### `post.html`

**Purpose:** Simple wrapper for individual posts

**What it does:** Specifies that posts should use the `default.html` layout

**Content:**

```yaml
---
layout: default
---
```

This is just a minimal file that tells Jekyll: "use the default layout for all posts."

## When to Edit Layouts

**Edit `default.html` when you want to:**

- Change the overall page structure
- Add/remove project sections
- Modify the header or footer
- Change how projects are displayed

**Don't edit layouts for:**

- Your bio text → Edit `_includes/bio.html` instead
- Project content → Edit files in `_posts/` instead
- Colors/fonts → Edit `style.scss` and `_sass/` files instead

## Layout Hierarchy

```
post.html
    ↓ uses
default.html (contains everything)
```

## Jekyll Layout Variables

Layouts can use variables from `_config.yml`:

- `{{ site.name }}` - Your name
- `{{ site.url }}` - Website URL
- `{{ site.baseurl }}` - Base path

And from individual posts:

- `{{ post.title }}` - Project title
- `{{ post.date }}` - Project date
- `{{ post.excerpt }}` - Project description
