# 02. Jsx Syntax And Rules

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can build predictable, composable user interfaces from small components and explicit state. The focus is **Jsx Syntax And Rules**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Components are pure descriptions of UI for given props and state.
- Keep state close to the components that use it, then lift it only when siblings must coordinate.
- Prefer composition—children, props, and custom hooks—over inheritance.

## Practical TypeScript example

```tsx
type ProfileProps = { name: string };

export function Profile({ name }: ProfileProps) {
  return <section><h2>{name}</h2><p>Welcome back.</p></section>;
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

Build a small **Jsx Syntax And Rules** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Jsx Syntax And Rules?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
