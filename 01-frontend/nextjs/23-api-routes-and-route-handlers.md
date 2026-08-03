# API Routes and Route Handlers

In the App Router, a route.ts file inside an app folder defines a Route Handler - a server-only endpoint exporting functions named after HTTP methods (GET, POST, etc.), replacing the Pages Router's api/ folder convention.

```javascript
// app/api/users/route.ts
export async function GET(request) {
  const users = await db.users.findMany();
  return Response.json(users);
}
```

**Key takeaway:** Route Handlers and Server Actions overlap in purpose - use Route Handlers when you need a real, externally callable REST endpoint, and Server Actions for form-driven mutations from within your own app.
