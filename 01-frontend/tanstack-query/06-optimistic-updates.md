# 06. Optimistic Updates

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can treat server data as a cached, asynchronous resource rather than ordinary component state. The focus is **Optimistic Updates**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Query data is server state: it can become stale, fail, be refetched, and be shared across components.
- A query key describes the exact resource; include every input that changes the result.
- Mutations change server data; invalidate or update the affected cached queries afterward.

## Practical TypeScript example

```tsx
import { useQuery } from "@tanstack/react-query";

type Todo = { id: string; title: string };
const getTodos = async (): Promise<Todo[]> => (await fetch("/api/todos")).json();
export function Todos() {
  const { data = [], isPending, error } = useQuery({ queryKey: ["todos"], queryFn: getTodos });
  if (isPending) return <p>Loading…</p>;
  if (error) return <p>Could not load todos.</p>;
  return <ul>{data.map(todo => <li key={todo.id}>{todo.title}</li>)}</ul>;
}
```

The query function returns a promise, and the query key is the cache address. Render pending, error, and success states explicitly so the UI never lies about the request.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Using a query key that omits a filter, user, locale, or other result-changing input.
- Copying query data into local state without a clear editing reason.
- Assuming `staleTime` means data is never refetched.

## Try it yourself

Build a small **Optimistic Updates** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Optimistic Updates?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
