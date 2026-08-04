# 04. Responsive Design With Breakpoint Prefixes

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can build responsive interfaces quickly with consistent, token-driven utility classes. The focus is **Responsive Design With Breakpoint Prefixes**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Utilities encode one visual concern at a time, which keeps styling near the markup it serves.
- Start mobile-first; add responsive prefixes only as content requires more space.
- Use the theme as the source of colors, spacing, radii, typography, and semantic design tokens.

## Practical TypeScript example

```tsx
<section className="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3">
  <article className="rounded-lg border p-4">Responsive card</article>
</section>
```

The class list is mobile-first and uses semantic project tokens where possible. Extract a React component when structure or behavior repeats—not merely because a few utilities repeat.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Building class names dynamically (`bg-${color}-500`), which the compiler cannot detect reliably.
- Using arbitrary values for ordinary design tokens.
- Packing page-sized markup into one component instead of extracting meaningful UI units.

## Try it yourself

Build a small **Responsive Design With Breakpoint Prefixes** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Responsive Design With Breakpoint Prefixes?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
