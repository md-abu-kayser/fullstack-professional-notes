# Combinators: Descendant, Child, Sibling

Combinators let you target elements based on their relationship to another. A space means "any descendant" (nav a), > means "direct child only" (ul > li), + means "immediately following sibling" (h2 + p), and ~ means "any following sibling" (h2 ~ p).

```css
nav a { color: white; }        /* any anchor inside nav */
ul > li { list-style: none; }  /* only direct li children */
h2 + p { margin-top: 0; }      /* paragraph right after an h2 */
```

**Key takeaway:** The direct child combinator (>) is invaluable for preventing styles from leaking into deeply nested, unrelated elements.
