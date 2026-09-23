# Login Page

A single-page login form built with plain HTML and CSS. No frameworks, no build step — open `index.html` in a browser and it works.

## Files

- `index.html` — page markup and form structure
- `style.css` — layout, colors, and responsive rules

## Features

- Email and password fields with browser-native validation (`required`, `type="email"`, `autocomplete`)
- "Forgot password?" link next to the password label
- Focus states on inputs and links, with a visible outline for keyboard navigation
- Responsive layout: the card shrinks its padding and heading size below 520px width
- Radial gradient background behind a white card, using CSS custom properties for color

## Customization

Colors, spacing, and radius values are defined as CSS variables at the top of `style.css`:

```css
:root {
  --page-bg: #0b0d12;
  --card-bg: #ffffff;
  --text: #17181c;
  --muted: #6d7179;
  --border: #dfe1e6;
  --input-bg: #fafafa;
  --accent: #6d4aff;
  --accent-dark: #5536db;
  --white: #ffffff;
}
```

Change these to re-theme the page without touching the rest of the stylesheet.

## Known limitations

- The form's `action="#"` and `method="post"` are placeholders — there's no backend wired up yet, so submitting the form won't do anything.
- No client-side JS: password visibility toggle, inline error messages, and "remember me" would all need to be added separately.

## Browser support

Uses standard flexbox, grid (`place-items`), and `:focus-visible`. Works in any current browser; `:focus-visible` isn't supported in old Safari (pre-15.4) or IE.
