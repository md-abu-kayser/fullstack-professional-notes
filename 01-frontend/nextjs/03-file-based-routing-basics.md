# File-based Routing Basics

In the App Router, folders define URL segments and a page.tsx file inside a folder makes that segment a publicly reachable route. A folder without a page.tsx is not directly routable - it only contributes to the URL path or holds shared layout/logic for its children.

```
app/
  dashboard/
    page.tsx        -> /dashboard
    settings/
      page.tsx       -> /dashboard/settings
```

**Key takeaway:** Only page.tsx (or route.ts for APIs) makes a folder segment actually reachable as a URL - layout.tsx, loading.tsx, etc. do not create routes on their own.
