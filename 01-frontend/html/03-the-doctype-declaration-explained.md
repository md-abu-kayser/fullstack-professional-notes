# The DOCTYPE Declaration Explained

The doctype declaration tells the browser to render the page in "standards mode" using the HTML5 specification, rather than falling back to quirks mode (an older, inconsistent rendering mode browsers use for legacy pages without a doctype). It is not an HTML tag - it is an instruction to the parser and must be the very first line of the document.

```html
<!DOCTYPE html>
```

**Key takeaway:** Missing the doctype can silently break your CSS box model calculations in quirks mode.
