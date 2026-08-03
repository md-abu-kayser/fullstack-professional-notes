# CommonJS vs ES Modules

CommonJS (require/module.exports) is Node.js's original, synchronous module system. ES Modules (import/export) are the standardized, asynchronous-capable system now supported natively in both Node and browsers. Node projects increasingly default to ES Modules, though many packages and configs still use CommonJS.

```javascript
// CommonJS
const { readFile } = require("fs");
module.exports = { myFunction };

// ES Modules
import { readFile } from "fs";
export { myFunction };
```

**Key takeaway:** You generally cannot mix require and import freely in the same file - the module system is set per-file or per-project via package.json's "type" field.
