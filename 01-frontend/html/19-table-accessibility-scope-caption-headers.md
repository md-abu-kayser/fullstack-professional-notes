# Table Accessibility: scope, caption, headers

The scope attribute on a th (scope="col" or scope="row") tells screen readers which cells a header applies to. caption gives the whole table a title, announced before the reader dives into the data. For complex tables with merged cells, the headers attribute on td can explicitly reference multiple th ids.

```html
<table>
  <caption>Q3 Sales by Region</caption>
  <tr><th scope="col">Region</th><th scope="col">Total</th></tr>
</table>
```

**Key takeaway:** Without scope, screen readers cannot reliably announce which header a data cell belongs to.
