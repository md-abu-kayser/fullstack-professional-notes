# Canvas Basics

canvas provides a blank, scriptable drawing surface rendered pixel by pixel via JavaScript, usually the 2D context or WebGL for 3D. Unlike SVG, canvas content is not part of the DOM - the browser has no memory of individual shapes once drawn, only the final pixel output.

```html
<canvas id="board" width="300" height="150"></canvas>
<script>
  const ctx = document.getElementById("board").getContext("2d");
  ctx.fillRect(10, 10, 100, 50);
</script>
```

**Key takeaway:** Because canvas has no DOM nodes for shapes, individual elements are not accessible or stylable via CSS.
