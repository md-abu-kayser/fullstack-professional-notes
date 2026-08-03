# Anchor Tags and the href Attribute

The a tag creates a hyperlink, with href pointing to the destination - a URL, an in-page anchor, an email address, or a phone number. Anchors are keyboard-focusable by default, which is why they should be used for navigation instead of clickable divs.

```html
<a href="#pricing">Jump to Pricing</a>
<a href="mailto:hello@example.com">Email us</a>
```

**Key takeaway:** An anchor without a valid href is not keyboard-focusable - it stops behaving like a link.
