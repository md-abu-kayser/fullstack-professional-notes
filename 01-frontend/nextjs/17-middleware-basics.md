# Middleware Basics

Middleware runs before a request completes, at the edge, letting you inspect or rewrite requests, redirect based on cookies or headers, or enforce authentication checks before a page even starts rendering. It is defined once in a middleware.ts file at the project root.

```javascript
export function middleware(request) {
  const isLoggedIn = request.cookies.has("session");
  if (!isLoggedIn) {
    return NextResponse.redirect(new URL("/login", request.url));
  }
}
export const config = { matcher: ["/dashboard/:path*"] };
```

**Key takeaway:** Middleware runs on every matched request, including static assets by default unless the matcher config excludes them - scope the matcher carefully to avoid unnecessary overhead.
