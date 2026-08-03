# ES Modules: import and export

ES Modules are the standard, browser-native module system, using export to expose values from a file and import to bring them into another. Unlike CommonJS, ES Modules are statically analyzable, enabling tree-shaking (removing unused exports) by bundlers.

```javascript
// math.js
export function add(a, b) { return a + b; }
export default function multiply(a, b) { return a * b; }

// app.js
import multiply, { add } from "./math.js";
```

**Key takeaway:** A file can have only one default export but any number of named exports - mixing both in one file is completely valid.
