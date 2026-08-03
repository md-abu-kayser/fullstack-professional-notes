# ARIA Roles and Accessible Rich Internet Applications

ARIA attributes fill accessibility gaps when native HTML cannot fully describe custom widgets - role redefines what an element is announced as, aria-label provides an accessible name, and aria-expanded communicates toggle state on things like custom dropdowns.

```html
<div role="button" tabindex="0" aria-pressed="false">Toggle</div>
```

**Key takeaway:** The first rule of ARIA is: if a native HTML element already does the job, use that instead.
