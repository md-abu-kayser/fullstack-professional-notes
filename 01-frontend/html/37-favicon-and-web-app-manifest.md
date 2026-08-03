# Favicon and Web App Manifest

The favicon is the small icon shown in browser tabs and bookmarks, linked via a link rel icon tag. The web app manifest, a JSON file linked with rel manifest, describes how a site behaves when installed as a Progressive Web App - its name, icons, theme color, and display mode.

```html
<link rel="icon" href="/favicon.ico">
<link rel="manifest" href="/site.webmanifest">
```

**Key takeaway:** A manifest is what makes "Add to Home Screen" produce an app-like icon instead of a bookmark shortcut.
