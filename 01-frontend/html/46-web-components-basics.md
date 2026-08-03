# Web Components Basics

Web Components let you build reusable custom HTML elements with encapsulated markup, styles, and behavior. Three technologies work together: Custom Elements define new tags, Shadow DOM encapsulates internal markup and CSS from the rest of the page, and HTML Templates provide reusable, inert markup fragments.

```html
<template id="my-card">
  <style>.card { border: 1px solid #ccc; }</style>
  <div class="card"><slot></slot></div>
</template>
```

**Key takeaway:** Shadow DOM styles do not leak out, and outside styles do not leak in - true encapsulation.
