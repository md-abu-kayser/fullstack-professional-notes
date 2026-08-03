# Custom Scrollbar Styling

Modern browsers support customizing scrollbar appearance via the ::-webkit-scrollbar pseudo-elements (Chrome/Safari/Edge) or the standard scrollbar-width and scrollbar-color properties (Firefox and now broadly supported). Overuse can hurt usability, so most teams apply it sparingly.

```css
.panel { scrollbar-width: thin; scrollbar-color: #999 transparent; }
.panel::-webkit-scrollbar { width: 8px; }
.panel::-webkit-scrollbar-thumb { background: #999; border-radius: 4px; }
```

**Key takeaway:** Always test custom scrollbars in more than one browser engine - the two approaches do not fully overlap in what they support.
