# Character Encoding and the charset Meta Tag

The charset meta tag declares the character encoding used to interpret the document's bytes - almost always UTF-8 today, which supports virtually every language and symbol. It must appear within the first 1024 bytes of the document, which is why it is always placed immediately inside head.

```html
<meta charset="UTF-8">
```

**Key takeaway:** Without a declared charset, browsers guess the encoding, which can corrupt special characters unpredictably.
