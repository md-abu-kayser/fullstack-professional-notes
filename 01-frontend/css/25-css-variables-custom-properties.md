# CSS Variables (Custom Properties)

Custom properties, written as --name and read with var(--name), let you define reusable values once and reference them throughout a stylesheet. Unlike Sass variables, they are live in the browser, can be changed with JavaScript, and respect the cascade - meaning they can be overridden per component or per theme.

```css
:root { --primary-color: #2563eb; --spacing-unit: 8px; }
.button { background: var(--primary-color); padding: var(--spacing-unit); }
```

**Key takeaway:** Because custom properties cascade, redefining --primary-color inside a .dark-theme class is all it takes to theme an entire site.
