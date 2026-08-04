# 08. Rendering Lists And The Key Prop

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can build predictable, composable user interfaces from small components and explicit state. The focus is **Rendering Lists And The Key Prop**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- A key identifies a list item across renders; it is not passed to the component as a prop.
- Use a stable record ID, never an array index when items can be reordered, added, or removed.
- Unstable keys cause lost input state and confusing UI bugs.

## Practical TypeScript example

```tsx
type Task = { id: string; title: string };
function TaskList({ tasks }: { tasks: Task[] }) {
  return <ul>{tasks.map(task => <li key={task.id}>{task.title}</li>)}</ul>;
}
```

TypeScript makes the component contract explicit. React reads props and state during render, then commits the minimal DOM change needed to reflect the returned JSX.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Mutating state objects or arrays in place.
- Using an Effect to coordinate ordinary render logic.
- Using list indexes as keys for editable or reorderable items.

## Try it yourself

Build a small **Rendering Lists And The Key Prop** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Rendering Lists And The Key Prop?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
