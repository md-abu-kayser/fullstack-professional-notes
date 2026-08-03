# When to Use the use client Directive

The "use client" directive at the top of a file marks that component (and everything it imports) as a Client Component, enabling hooks like useState and useEffect, and browser-only APIs. It should be placed as low in the component tree as possible - on the interactive leaf, not the whole page - to keep the client bundle small.

```jsx
"use client";
import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);
  return <button onClick={() => setCount(count + 1)}>{count}</button>;
}
```

**Key takeaway:** Marking a high-level layout or page as "use client" unnecessarily forces every child component into the client bundle too, even ones that did not need it.
