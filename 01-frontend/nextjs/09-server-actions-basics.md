# Server Actions Basics

Server Actions are async functions marked with "use server" that run exclusively on the server but can be called directly from Client or Server Components, including as a form's action - eliminating the need to manually create an API route for simple mutations.

```jsx
async function createPost(formData) {
  "use server";
  await db.posts.create({ title: formData.get("title") });
}
```

**Key takeaway:** Server Actions are called over the network like an API endpoint under the hood, so the same authentication and validation discipline as any other server entry point still applies.
