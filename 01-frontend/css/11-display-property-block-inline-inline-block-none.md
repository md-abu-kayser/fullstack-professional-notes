# Display Property: block, inline, inline-block, none

display controls how an element participates in layout. block takes the full available width and starts a new line. inline flows with text and ignores width/height. inline-block flows with text like inline but respects width, height, and vertical margin like block. none removes the element from layout entirely, as if it did not exist.

```css
.badge { display: inline-block; width: 80px; padding: 4px; }
.hidden { display: none; }
```

**Key takeaway:** display: none removes an element from the accessibility tree too - screen readers skip it entirely, unlike visibility: hidden.
