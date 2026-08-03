# The track Element for Captions and Subtitles

track is nested inside audio or video to add timed text tracks - captions, subtitles, or chapters - sourced from a separate WebVTT file. This is essential for accessibility and is increasingly a legal requirement for public-facing video content.

```html
<video controls>
  <source src="clip.mp4" type="video/mp4">
  <track src="captions-en.vtt" kind="captions" srclang="en" label="English">
</video>
```

**Key takeaway:** kind="captions" includes sound-effect context; kind="subtitles" assumes the viewer can already hear audio.
