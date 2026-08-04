# 11. useEffect Basics And Dependency Array

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can build predictable, composable user interfaces from small components and explicit state. The focus is **useEffect Basics And Dependency Array**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Effects synchronize React with something outside React (a subscription, timer, browser API, or network connection).
- Every reactive value used by the effect belongs in its dependency list; return a cleanup function for resources you start.
- Do not use an Effect to derive values that can be calculated during render.

## Practical TypeScript example

```tsx
useEffect(() => {
  const controller = new AbortController();
  void fetch(`/api/projects?team=${teamId}`, { signal: controller.signal })
    .then(response => response.json())
    .then(setProjects)
    .catch(error => { if (error.name !== "AbortError") setError(error); });
  return () => controller.abort();
}, [teamId]);
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

Build a small **useEffect Basics And Dependency Array** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about useEffect Basics And Dependency Array?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
