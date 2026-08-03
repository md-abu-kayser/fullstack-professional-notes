# Content-box vs Border-box

box-sizing: content-box (the default) means width/height apply only to the content area - padding and border are added on top, growing the box. box-sizing: border-box means width/height include padding and border, so the box stays the size you set.

```css
* { box-sizing: border-box; }
.card { width: 300px; padding: 20px; } /* stays exactly 300px wide */
```

**Key takeaway:** Nearly every modern CSS reset sets border-box globally - it is one of the highest-value one-liners in any project.
