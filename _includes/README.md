# Includes Folder

This folder contains reusable HTML components that can be included in multiple pages.

## Why Use Includes?

Includes let you write content once and reuse it everywhere. When you update an include, it automatically updates across all pages that use it.

## Current Includes

### `name.html`

**Purpose:** Your name displayed in the header

**Used in:**

- `index.html` (homepage)
- `_layouts/default.html` (project pages)

**To edit:** Simply open `name.html` and change the text. Your name will update everywhere automatically.

**Format:** Plain text (no HTML tags needed)

### `bio.html`

**Purpose:** Your biography text

**Used in:**

- `index.html` (homepage)
- `_layouts/default.html` (project pages)

**To edit:** Simply open `bio.html` and change the text. Your bio will update everywhere automatically.

**Format:** Plain HTML paragraphs (`<p>` tags with links `<a>`)

## Adding New Includes

If you have content that appears in multiple places, create an include:

1. Create a new file: `component-name.html`
2. Add your HTML content
3. Use it anywhere with: `{% include component-name.html %}`

## Examples

**Social links include:**

```html
<!-- _includes/social-links.html -->
<p>
  <a href="mailto:your@email.com">Email</a> /
  <a href="https://linkedin.com/...">LinkedIn</a>
</p>
```

**Use it:**

```html
{% include social-links.html %}
```
