# Preprocessors: Sass Basics

Sass extends CSS with features the language lacks natively (or lacked, before custom properties): nesting selectors, variables, mixins for reusable style blocks, and functions - all compiled down to plain CSS before shipping to the browser.

```scss
$primary: #2563eb;

.card {
  padding: 16px;
  &:hover { border-color: $primary; }
  .title { font-weight: bold; }
}
```

**Key takeaway:** Native CSS variables and nesting have closed much of the gap with Sass, but mixins and functions still make Sass valuable in larger codebases.
