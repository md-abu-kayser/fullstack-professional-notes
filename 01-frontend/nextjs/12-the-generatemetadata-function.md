# The generateMetadata Function

When metadata depends on dynamic data (like a blog post's title fetched from a database), generateMetadata is an async function that computes it per-request, replacing the static metadata export for that route.

```jsx
export async function generateMetadata({ params }) {
  const post = await getPost(params.slug);
  return { title: post.title, description: post.excerpt };
}
```

**Key takeaway:** Next.js automatically deduplicates the data fetch inside generateMetadata with an identical fetch inside the page component itself, so you rarely pay for the request twice.
