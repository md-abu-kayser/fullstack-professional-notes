# Responsive Images with srcset and sizes

srcset lets the browser choose the best image file for the current screen size and pixel density from a list of candidates, while sizes tells it how much space the image will occupy at different viewport widths. This avoids shipping a huge desktop image to a small phone screen.

```html
<img src="small.jpg"
     srcset="small.jpg 480w, medium.jpg 800w, large.jpg 1200w"
     sizes="(max-width: 600px) 480px, 800px"
     alt="Product photo">
```

**Key takeaway:** srcset saves bandwidth; the browser, not your CSS, decides which file to fetch.
