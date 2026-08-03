# audio and video Elements

Both elements embed native media players without any plugins. The controls attribute shows play, pause, and volume UI, multiple source children let the browser pick a supported format, and autoplay should generally be avoided or paired with muted to respect user experience norms.

```html
<video controls width="480">
  <source src="clip.mp4" type="video/mp4">
  <source src="clip.webm" type="video/webm">
</video>
```

**Key takeaway:** Most browsers block unmuted autoplay outright - never rely on it for anything essential.
