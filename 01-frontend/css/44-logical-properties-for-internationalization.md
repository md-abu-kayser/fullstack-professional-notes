# Logical Properties for Internationalization

Logical properties like margin-inline-start or padding-block-end describe spacing relative to text flow direction rather than fixed physical directions like left/right. In a right-to-left language, "inline-start" automatically flips to the right, without needing a separate RTL stylesheet.

```css
.card { margin-inline: 16px; padding-block: 8px; }
```

**Key takeaway:** Adopting logical properties from the start is far cheaper than retrofitting RTL support into a codebase built entirely on left/right physical properties.
