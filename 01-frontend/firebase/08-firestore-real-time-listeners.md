# 08. Firestore Real Time Listeners

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can connect a browser app to Firebase while protecting user data with server-enforced rules. The focus is **Firestore Real Time Listeners**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- A collection contains documents; documents are small JSON-like records that can contain subcollections.
- Model for the queries your UI needs. Denormalize selected fields when it removes costly client joins.
- Use `serverTimestamp()` for trusted timestamps and pagination cursors for growing lists.

## Practical TypeScript example

```tsx
import { collection, onSnapshot, query, where } from "firebase/firestore";

const unsubscribe = onSnapshot(query(collection(db, "tasks"), where("ownerId", "==", uid)), snapshot => {
  setTasks(snapshot.docs.map(doc => ({ id: doc.id, ...doc.data() })));
});
// Call unsubscribe when the component or subscription is no longer needed.
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

Build a small **Firestore Real Time Listeners** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Firestore Real Time Listeners?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
