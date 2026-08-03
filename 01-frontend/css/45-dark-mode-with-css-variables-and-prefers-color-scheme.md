# Dark Mode with CSS Variables and prefers-color-scheme

prefers-color-scheme is a media query that detects the user's OS-level light/dark preference. Combined with CSS custom properties, it becomes trivial to theme an entire site by redefining a small set of variables inside the media query, or a manual toggle class.

```css
:root { --bg: #ffffff; --text: #111111; }

@media (prefers-color-scheme: dark) {
  :root { --bg: #111111; --text: #f5f5f5; }
}

body { background: var(--bg); color: var(--text); }
```

**Key takeaway:** Supporting both automatic (media query) and manual (toggle class) dark mode gives users control without doubling your CSS.
