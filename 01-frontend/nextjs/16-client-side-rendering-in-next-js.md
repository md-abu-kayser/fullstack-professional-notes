# Client-Side Rendering in Next.js

Some data genuinely belongs on the client - data that changes based on user interaction after the page has loaded, like a live search or a polling dashboard widget. In these cases, a Client Component using useEffect or a data-fetching library like TanStack Query is still the right tool, even inside an otherwise server-rendered app.

```jsx
"use client";
import { useQuery } from "@tanstack/react-query";

export default function LiveTicker() {
  const { data } = useQuery({ queryKey: ["price"], queryFn: fetchPrice });
  return <span>{data?.price}</span>;
}
```

**Key takeaway:** Client-side rendering is not "wrong" in Next.js - it is simply reserved for genuinely client-driven, frequently changing data rather than the default for everything.
