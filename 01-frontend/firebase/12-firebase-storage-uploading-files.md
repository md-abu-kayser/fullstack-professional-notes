# 12. Firebase Storage Uploading Files

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can connect a browser app to Firebase while protecting user data with server-enforced rules. The focus is **Firebase Storage Uploading Files**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Firebase offers managed backend services that work directly from web and mobile clients.
- Use the modular SDK so bundlers can tree-shake unused services.
- Keep client SDK usage separate from privileged Admin SDK code.

## Practical TypeScript example

```tsx
// lib/firebase.ts
import { getApp, getApps, initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";

const config = { apiKey: process.env.NEXT_PUBLIC_FIREBASE_API_KEY! };
const app = getApps().length ? getApp() : initializeApp(config);
export const auth = getAuth(app);
```

The example uses the modular Firebase API. In a Next.js project, initialize the browser SDK once, keep only `NEXT_PUBLIC_` configuration on the client, and use an Admin SDK or a trusted backend for privileged work.

## Production checklist

- Name state, events, and UI states after the user’s domain—not after an implementation detail.
- Include loading, empty, error, and success states where data or user actions are involved.
- Test keyboard interaction, small screens, and the failure path before calling a screen complete.
- Keep secrets on the server; validate and authorize at the boundary that protects the data.

## Common mistakes

- Shipping permissive production rules such as `allow read, write: if true`.
- Trusting a client-supplied owner ID without checking it in a rule.
- Putting Admin SDK credentials or service-account JSON in client code.

## Try it yourself

Build a small **Firebase Storage Uploading Files** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Firebase Storage Uploading Files?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
