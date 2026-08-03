# Aspect-ratio Property

aspect-ratio locks the ratio between an element's width and height, so setting only one dimension automatically derives the other. This replaced older padding-percentage hacks that were previously needed to reserve space for responsive images and videos before they loaded.

```css
.video-embed { aspect-ratio: 16 / 9; width: 100%; }
```

**Key takeaway:** Setting aspect-ratio on images and iframes prevents layout shift while the actual content is still loading - a direct Core Web Vitals win.
