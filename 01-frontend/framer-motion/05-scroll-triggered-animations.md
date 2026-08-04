# 05. Scroll Triggered Animations

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can add intentional animation that explains state changes without slowing down the interface. The focus is **Scroll Triggered Animations**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Use Motion when movement communicates hierarchy, continuity, feedback, or a state change—not merely decoration.
- Animate `transform` and `opacity` first; these are usually the least expensive properties to animate.
- Respect `prefers-reduced-motion` and keep enter/exit motion short and interruptible.

## Practical TypeScript example

```tsx
"use client";
import { motion } from "motion/react";

export function SaveButton() {
  return <motion.button whileHover={{ scale: 1.03 }} whileTap={{ scale: 0.97 }}>Save</motion.button>;
}
```

The motion component behaves like its HTML counterpart, with animation props added. In the Next.js App Router, interactive Motion components normally belong in a client component.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Animating layout-affecting properties on many elements without profiling.
- Using a different `key` between presence renders, which prevents the expected exit animation.
- Ignoring reduced-motion preferences or making required content hard to reach while moving.

## Try it yourself

Build a small **Scroll Triggered Animations** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Scroll Triggered Animations?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
