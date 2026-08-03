# CSS Modules Overview

CSS Modules automatically scope class names to the component that imports them, appending a unique hash at build time - so .button in one file never collides with .button in another. This gives the safety of scoped styles without needing a CSS-in-JS runtime.

```css
/* Button.module.css */
.button { padding: 8px 16px; }
```

```jsx
import styles from "./Button.module.css";
<button className={styles.button}>Click</button>
```

**Key takeaway:** Because the class name is just a plain string at runtime, CSS Modules add zero runtime overhead compared to CSS-in-JS solutions.
