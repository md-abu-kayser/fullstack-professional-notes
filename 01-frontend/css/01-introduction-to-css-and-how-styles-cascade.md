# Introduction to CSS and How Styles Cascade

CSS (Cascading Style Sheets) controls the visual presentation of HTML - colors, layout, typography, spacing. The "cascade" in its name describes how multiple rules can target the same element, with the browser resolving conflicts using a defined order: source order, specificity, and importance. Understanding the cascade is the single most useful mental model for debugging why a style is not applying the way you expect.

```css
p { color: blue; }
p { color: red; } /* This wins - later rule, same specificity */
```

**Key takeaway:** When two rules of equal specificity conflict, the one that appears later in the stylesheet wins.

**Interview angle:** Be ready to explain the three cascade tiebreakers in order: source order, specificity, then `!important`.
