# Server Components vs Client Components

By default, every component in the App Router is a Server Component - rendered on the server, sending zero JavaScript to the browser for that component. Client Components (marked with "use client") are needed only when a component uses hooks, browser APIs, or event handlers like onClick.

```jsx
// Server Component (default) - can be async, can fetch data directly
export default async function ProductList() {
  const products = await getProducts();
  return <ul>{products.map(p => <li key={p.id}>{p.name}</li>)}</ul>;
}
```

**Key takeaway:** Server Components reduce shipped JavaScript significantly - default to them, and only opt into "use client" for the specific interactive leaves of the tree.
