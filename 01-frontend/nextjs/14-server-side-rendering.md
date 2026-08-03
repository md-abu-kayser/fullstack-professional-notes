# Server-Side Rendering

Server-Side Rendering generates the HTML for a page on-demand, per request, on the server - necessary when content is personalized (a logged-in user's dashboard) or must always reflect the very latest data. It is slower per-request than static generation but keeps data fresh.

```jsx
export default async function Page() {
  const data = await fetch("https://api.example.com/live-data", { cache: "no-store" });
  return <Dashboard data={data} />;
}
```

**Key takeaway:** Setting cache: "no-store" on a fetch (or using cookies/headers) opts a route out of static generation and into per-request server rendering.
