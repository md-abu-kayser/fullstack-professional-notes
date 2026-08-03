# CSS Architecture: Utility-First vs Component-Based

Component-based CSS (like BEM or CSS Modules) writes semantic class names tied to what a component is. Utility-first CSS (like Tailwind) composes many small, single-purpose classes directly in markup. Utility-first trades some HTML verbosity for far less CSS to maintain and near-zero specificity conflicts.

```html
<!-- Component-based -->
<div class="card card--featured">...</div>

<!-- Utility-first -->
<div class="rounded-lg shadow-md p-4 border-2 border-blue-500">...</div>
```

**Key takeaway:** Neither approach is objectively better - the right choice depends on team size, design system maturity, and how much the design changes over time.
