# Environment Variables in Next.js

Environment variables in a .env.local file are available server-side by default. Only variables explicitly prefixed with NEXT_PUBLIC_ are exposed to the browser bundle - everything else stays server-only, which is an important security boundary to keep in mind.

```
DATABASE_URL=postgres://...          # server-only
NEXT_PUBLIC_API_URL=https://api.com  # exposed to the browser
```

**Key takeaway:** Never prefix a secret (API key, database credential) with NEXT_PUBLIC_ - that prefix is precisely what makes a variable ship inside the client-side JavaScript bundle.
