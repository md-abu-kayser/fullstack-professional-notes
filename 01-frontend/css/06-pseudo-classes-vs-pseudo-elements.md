# Pseudo-classes vs Pseudo-elements

Pseudo-classes (single colon, like :hover, :focus, :nth-child) target an element in a particular state or position. Pseudo-elements (double colon, like ::before, ::after, ::first-line) target a sub-part of an element that is not a real DOM node.

```css
button:hover { background: navy; }
li:nth-child(odd) { background: #f5f5f5; }
p::first-line { font-weight: bold; }
.tooltip::after { content: "!"; }
```

**Key takeaway:** ::before and ::after require a content property to render at all, even if it is just an empty string.
