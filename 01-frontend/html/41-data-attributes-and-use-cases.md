# Data Attributes and Use Cases

data-* attributes let you attach arbitrary metadata to HTML elements that JavaScript can read via the dataset property, without resorting to non-standard attributes or hidden inputs. They are commonly used to pass server-rendered values to client-side scripts.

```html
<button data-product-id="482" data-in-stock="true">Add to Cart</button>
<script>
  console.log(button.dataset.productId);
</script>
```

**Key takeaway:** dataset automatically converts a hyphenated attribute name to camelCase in JavaScript.
