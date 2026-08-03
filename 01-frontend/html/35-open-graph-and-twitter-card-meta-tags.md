# Open Graph and Twitter Card Meta Tags

Open Graph tags control how a link looks when shared on Facebook, LinkedIn, and most messaging apps - the preview image, title, and description. Twitter has its own similar set of tags, which falls back to Open Graph tags if absent.

```html
<meta property="og:title" content="My Article Title">
<meta property="og:image" content="https://example.com/preview.jpg">
<meta name="twitter:card" content="summary_large_image">
```

**Key takeaway:** Without an og:image, most platforms show a blank or generic preview when your link is shared.
