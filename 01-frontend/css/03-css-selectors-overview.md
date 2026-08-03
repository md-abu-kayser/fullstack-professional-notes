# CSS Selectors Overview

Selectors decide which elements a rule applies to. Common types include the type selector (p), class selector (.card), ID selector (#header), universal selector (*), and attribute selectors ([type="text"]). Combining selectors gets more specific and powerful the deeper your project grows.

```css
.card { border-radius: 8px; }
#main-header { font-weight: bold; }
input[type="email"] { border-color: teal; }
```

**Key takeaway:** Prefer classes over IDs for styling - IDs carry much higher specificity, which makes overriding them later painful.
