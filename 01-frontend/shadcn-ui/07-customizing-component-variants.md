# 07. Customizing Component Variants

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can assemble accessible product UI from code you own and can tailor to the design system. The focus is **Customizing Component Variants**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- shadcn/ui copies component source into your project; it is not a hosted component package runtime.
- The components are built from accessible primitives and Tailwind styles, but your product still owns accessibility decisions.
- Customize tokens and variants at the design-system level before editing individual screens.

## Practical TypeScript example

```tsx
const buttonVariants = cva("inline-flex items-center justify-center rounded-md text-sm font-medium", {
  variants: { variant: { brand: "bg-indigo-600 text-white hover:bg-indigo-700", ghost: "hover:bg-muted" }, size: { sm: "h-8 px-3", md: "h-10 px-4" } },
  defaultVariants: { variant: "brand", size: "md" },
});
```

This is ordinary project code after installation. Keep presentation components reusable, then compose them in feature-level components that contain business logic.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Treating generated component code as untouchable dependency code.
- Skipping dialog labels, descriptions, keyboard testing, or focus return.
- Hard-coding colors across screens instead of using design tokens.

## Try it yourself

Build a small **Customizing Component Variants** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Customizing Component Variants?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
