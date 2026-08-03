# CSS Naming Convention Trade-offs in Real Projects

Choosing between BEM, utility-first (Tailwind), CSS Modules, or a custom convention is less about which is "correct" and more about team size, design system maturity, and tooling. BEM scales well without a build step; utility-first speeds up prototyping but increases HTML verbosity; CSS Modules give collision-safety with minimal ceremony.

```html
<!-- BEM -->
<div class="card card--featured"><h3 class="card__title">Title</h3></div>
```

**Key takeaway:** Consistency across a codebase matters more than which specific convention is chosen - mixing several approaches in one project is the real anti-pattern.
