# Writing Clean, Readable JavaScript

Clean JavaScript favors small, single-purpose functions, descriptive names over comments explaining what code does, early returns over deeply nested conditionals, and consistent formatting enforced by a linter and formatter (ESLint and Prettier) rather than manual style debates.

```javascript
// Instead of deep nesting
function processOrder(order) {
  if (!order) return;
  if (!order.isValid) return;
  // ...actual logic, not buried three levels deep
}
```

**Key takeaway:** A linter catching style and correctness issues automatically in CI is worth more in a real team than any individual's personal style preferences.
