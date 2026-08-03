# Transform Property: translate, scale, rotate

transform repositions, resizes, or rotates an element without affecting the layout of surrounding elements - unlike changing top/left or width/height directly. Multiple transforms can be combined in one declaration, applied in the order written.

```css
.card:hover {
  transform: translateY(-4px) scale(1.02) rotate(1deg);
}
```

**Key takeaway:** transform runs on the GPU compositor in most browsers, making it dramatically smoother for animation than properties that trigger layout or paint.
