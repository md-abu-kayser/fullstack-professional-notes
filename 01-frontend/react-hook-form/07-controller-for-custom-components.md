# 07. Controller For Custom Components

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can manage accessible forms with minimal re-rendering and reliable validation feedback. The focus is **Controller For Custom Components**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- React Hook Form stores most field values outside React state, reducing keystroke re-renders.
- `register` works with native/ref-forwarding inputs; use `Controller` for controlled third-party widgets.
- Show errors near the field, connect them with `aria-describedby`, and preserve the user’s entered values.

## Practical TypeScript example

```tsx
import { useForm } from "react-hook-form";

type ContactValues = { email: string };
const { register, handleSubmit, formState: { errors } } = useForm<ContactValues>();
const submit = (values: ContactValues) => console.log(values);
```

The generic makes field names type-safe. `handleSubmit` runs validation first; valid values reach the submit function, while `errors` drives accessible feedback in the UI.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Forgetting a `defaultValue` for controlled fields.
- Using `Controller` for an input that `register` already supports.
- Showing only color to communicate a validation error.

## Try it yourself

Build a small **Controller For Custom Components** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Controller For Custom Components?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
