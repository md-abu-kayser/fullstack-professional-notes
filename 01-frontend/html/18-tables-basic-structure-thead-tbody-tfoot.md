# Tables: Basic Structure (thead, tbody, tfoot)

A well-structured table uses table as the container, thead for header rows, tbody for the main data, and tfoot for summary rows like totals. th marks header cells and td marks data cells. This structure is what lets screen readers and CSS target sections independently.

```html
<table>
  <thead><tr><th>Name</th><th>Score</th></tr></thead>
  <tbody><tr><td>Alex</td><td>95</td></tr></tbody>
</table>
```

**Key takeaway:** Tables should be used for tabular data only, never for page layout.
