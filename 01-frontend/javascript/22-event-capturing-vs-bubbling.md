# Event Capturing vs Bubbling

Events travel through the DOM in three phases: capturing (top down, from document to target), target (the element itself), and bubbling (bottom up, back to document). Listeners run during bubbling by default; passing true (or {capture: true}) as the third argument to addEventListener runs it during capturing instead.

```javascript
parent.addEventListener("click", handler, { capture: true }); // capturing phase
child.addEventListener("click", handler); // bubbling phase (default)
```

**Key takeaway:** event.stopPropagation() halts further travel in whichever phase is currently running - it does not stop the default action, only the propagation.
