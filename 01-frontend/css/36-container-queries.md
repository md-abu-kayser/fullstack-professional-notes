# Container Queries

Container queries let an element's styles respond to the size of its containing element, rather than the size of the whole viewport - solving the long-standing problem of truly reusable components that need to look different in a narrow sidebar versus a wide main column.

```css
.card-container { container-type: inline-size; }

@container (min-width: 400px) {
  .card { display: flex; }
}
```

**Key takeaway:** Unlike media queries, container queries make the same component adapt correctly no matter where it is placed on the page.
