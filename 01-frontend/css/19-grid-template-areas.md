# Grid Template Areas

grid-template-areas lets you sketch a layout visually using named strings, then assign each child a grid-area matching a name. This makes complex layouts extremely readable, since the CSS itself looks like an ASCII wireframe of the page.

```css
.layout {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}
.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
```

**Key takeaway:** You can redefine grid-template-areas inside a media query to completely reflow the layout for mobile with almost no other changes.
