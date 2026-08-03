# HTML5 APIs Overview

Beyond markup, HTML5 introduced browser APIs accessible via JavaScript: the Geolocation API for location access, the Drag and Drop API for native drag interactions, the Web Storage API, and the History API for manipulating the URL without a full page reload.

```html
<div draggable="true" ondragstart="event.dataTransfer.setData('text', 'item')">Drag me</div>
```

**Key takeaway:** Most HTML5 APIs require user permission prompts or HTTPS to function in modern browsers.
