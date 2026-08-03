# Data Fetching in Server Components

Server Components can be async functions and fetch data directly with await, with no useEffect, loading state juggling, or client-side waterfall - the data is ready before the HTML is even sent to the browser. Next.js extends the native fetch with automatic request deduplication and caching controls.

```jsx
export default async function Page() {
  const res = await fetch("https://api.example.com/posts", {
    next: { revalidate: 3600 },
  });
  const posts = await res.json();
  return <PostList posts={posts} />;
}
```

**Key takeaway:** Multiple components requesting the same URL with fetch during one render are automatically deduplicated into a single request by Next.js.
