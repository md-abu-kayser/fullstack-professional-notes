# DOM Traversal: Parent, Child, Sibling

Once you have one DOM node, you can navigate relative to it: parentElement, children, firstElementChild/lastElementChild, and nextElementSibling/previousElementSibling. These "Element" variants skip text and comment nodes, unlike their non-Element counterparts.

```javascript
const item = document.querySelector(".item");
const parent = item.parentElement;
const next = item.nextElementSibling;
```

**Key takeaway:** Always prefer the Element-suffixed traversal properties - the plain versions (parentNode, nextSibling) also return whitespace text nodes, which usually is not what you want.
