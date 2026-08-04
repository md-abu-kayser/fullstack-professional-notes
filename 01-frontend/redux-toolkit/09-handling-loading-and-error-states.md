# 09. Handling Loading And Error States

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can organize shared client state with readable actions, slices, selectors, and async workflows. The focus is **Handling Loading And Error States**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Use Redux for shared client state with meaningful transitions—not for every input or server cache.
- A slice owns its initial state, reducers, generated action creators, and reducer export.
- Immer lets reducers use mutation-looking syntax safely; it produces immutable updates underneath.

## Practical TypeScript example

```tsx
import { createSlice, PayloadAction } from "@reduxjs/toolkit";

type CounterState = { value: number };
const initialState: CounterState = { value: 0 };
export const counterSlice = createSlice({
  name: "counter", initialState,
  reducers: { increment: state => { state.value += 1; }, set: (state, action: PayloadAction<number>) => { state.value = action.payload; } }
});
```

The reducer is a state transition: action in, next state out. Keep it deterministic; perform I/O in thunks, listeners, or a server-data layer.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Putting promises, class instances, or DOM nodes in Redux state.
- Using Redux to cache every server response instead of a query library.
- Writing reducers with hidden side effects or non-deterministic values.

## Try it yourself

Build a small **Handling Loading And Error States** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Handling Loading And Error States?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
