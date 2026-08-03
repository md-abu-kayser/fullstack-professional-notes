# Script Tag: async vs defer

By default, a script tag blocks HTML parsing until it downloads and executes. async downloads it in parallel and runs it as soon as it is ready, with order not guaranteed across multiple scripts. defer also downloads in parallel but waits to execute until after parsing finishes, in document order - generally the safer default.

```html
<script src="analytics.js" async></script>
<script src="app.js" defer></script>
```

**Key takeaway:** For scripts that depend on the DOM being fully parsed, defer is almost always the right choice.
