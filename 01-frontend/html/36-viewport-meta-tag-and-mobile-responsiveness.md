# Viewport Meta Tag and Mobile Responsiveness

The viewport meta tag tells mobile browsers how to scale the page instead of rendering it as a shrunk-down desktop layout. Without it, media queries will not behave as expected on phones at all.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Key takeaway:** This single tag is a prerequisite for any responsive CSS to work correctly on mobile devices.
