# Specificity and the Cascade Explained

Specificity is a scoring system browsers use to decide which rule wins when several target the same element. Roughly, inline styles score highest, then IDs, then classes/attributes/pseudo-classes, then element selectors. A higher-specificity selector always wins regardless of source order.

```css
#nav a { color: black; }     /* higher specificity */
.menu-link { color: blue; }  /* loses even if written later */
```

**Key takeaway:** Fighting specificity with more specific selectors (or worse, `!important`) is a code smell - it usually means the CSS architecture needs rethinking, not a stronger selector.
