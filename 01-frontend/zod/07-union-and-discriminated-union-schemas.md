# 07. Union And Discriminated Union Schemas

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can validate untrusted runtime data and derive TypeScript types from one source of truth. The focus is **Union And Discriminated Union Schemas**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- TypeScript checks compile time; Zod checks real values at runtime.
- Parse API input at boundaries, then let internal code operate on validated types.
- Use `safeParse` for user-facing errors and `parse` when an invalid value is a programmer or boundary failure.

## Practical TypeScript example

```tsx
const payment = z.discriminatedUnion("method", [
  z.object({ method: z.literal("card"), last4: z.string().length(4) }),
  z.object({ method: z.literal("bank"), iban: z.string().min(15) }),
]);
```

The schema validates the runtime value and `z.infer` keeps the TypeScript type synchronized. Keep schemas close to the API, form, or domain boundary they protect.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Using a type assertion instead of validation for API data.
- Running an async validation inside a synchronous parse path.
- Transforming untrusted values before first establishing their input type.

## Try it yourself

Build a small **Union And Discriminated Union Schemas** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Union And Discriminated Union Schemas?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
