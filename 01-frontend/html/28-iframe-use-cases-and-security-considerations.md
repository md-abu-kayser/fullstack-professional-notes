# iframe: Use Cases and Security Considerations

iframe embeds another HTML document inside the current page - common for embedding maps, videos, or payment widgets. Because it loads external content, it is also a security surface; the sandbox attribute restricts what the embedded page can do, and the allow attribute grants specific permissions like camera or fullscreen.

```html
<iframe src="https://example.com/widget" sandbox="allow-scripts" title="Widget"></iframe>
```

**Key takeaway:** Always add a title attribute to iframes - screen readers otherwise announce them as unlabeled.
