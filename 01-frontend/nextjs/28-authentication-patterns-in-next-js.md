# Authentication Patterns in Next.js

Common approaches include using a dedicated auth library (NextAuth.js/Auth.js) for OAuth and session management, checking authentication state in Middleware to protect whole route groups before rendering, and reading cookies directly in Server Components for per-request session checks.

```javascript
import { cookies } from "next/headers";

export default async function Page() {
  const session = cookies().get("session");
  if (!session) redirect("/login");
}
```

**Key takeaway:** Checking auth in Middleware protects a route before any rendering work happens at all, which is more efficient than letting a page start rendering and redirecting afterward.
