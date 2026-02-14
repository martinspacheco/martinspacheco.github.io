# Sass (Stylesheets) Folder

This folder contains modular CSS stylesheets written in SCSS (Sass) format. These files are compiled into the main `style.css` that styles your website.

## How It Works

The main file `style.scss` (in the root directory) imports all these partial files and compiles them into one CSS file.

## Current Style Files

### `_variables.scss`

**Purpose:** Define colors, fonts, and sizing variables

**Contains:**

- Color palette (primary, secondary, accent colors)
- Font families
- Size values (font sizes, spacing)
- Breakpoints for responsive design

**Edit this when:** You want to change colors, fonts, or overall design values

---

### `_reset.scss`

**Purpose:** Reset browser default styles for consistency

**Contains:**

- Removes default margins and padding
- Sets consistent box-sizing
- Normalizes form elements
- Ensures consistent rendering across browsers

**Edit this:** Rarely (only if you need to override specific browser defaults)

---

### `_highlights.scss`

**Purpose:** Syntax highlighting for code blocks

**Contains:**

- CSS for displaying code with syntax colors
- Styles for `<pre>` and `<code>` tags

**Edit this:** If you want to change how code appears on your site

---

### `_svg-icons.scss`

**Purpose:** Icon styles (social media icons, etc.)

**Contains:**

- Styling for SVG icons
- Icon sizing and colors
- Hover effects

**Edit this:** To change icon appearance or add new icon styles

---

## How Sass Compiles

```
style.scss (root folder)
    ↓ imports
_sass/_variables.scss
_sass/_reset.scss
_sass/_highlights.scss
_sass/_svg-icons.scss
    ↓ compiles to
style.css (served to browsers)
```

## Making Style Changes

### To Change Colors

1. Open `_sass/_variables.scss`
2. Change color values
3. Push changes (Jekyll auto-compiles on GitHub)

### To Add New Styles

1. Edit `style.scss` in the root folder
2. Or add new partial file: `_sass/_custom.scss`
3. Import in `style.scss`: `@import "custom";`

### Best Practices

- **Use variables:** Define colors/sizes once in `_variables.scss`, use everywhere
- **Keep organized:** Each file has a specific purpose
- **Test changes:** Preview locally before pushing
- **Comments:** Add comments explaining complex styles

## SCSS Features

SCSS extends CSS with useful features:

**Variables:**

```scss
$primary-color: #0891b2;
.button {
  background: $primary-color;
}
```

**Nesting:**

```scss
.container {
  padding: 20px;

  h1 {
    color: blue;
  }
  p {
    line-height: 1.7;
  }
}
```

**Imports:**

```scss
@import "variables";
@import "reset";
```

## Resources

- [Sass Documentation](https://sass-lang.com/documentation)
- [SCSS Syntax Guide](https://sass-lang.com/guide)
