# 10. Firestore Security Rules Basics

> **Level:** Beginner → production-minded  
> **Prerequisites:** JavaScript, TypeScript, and basic React/Next.js

## Why this matters

After this lesson, you can connect a browser app to Firebase while protecting user data with server-enforced rules. The focus is **Firestore Security Rules Basics**. A professional implementation makes the happy path clear, handles failure honestly, and remains understandable to the next developer.

## Core ideas

- Firebase client configuration is public by design; security comes from Authentication, Security Rules, and server-side checks.
- Rules are not filters. A query must satisfy the rule constraints before Firebase returns any documents.
- Test rules in the Emulator Suite before deployment and default to deny.

## Practical TypeScript example

```tsx
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /tasks/{taskId} {
      allow read: if request.auth != null && resource.data.ownerId == request.auth.uid;
      allow create: if request.auth != null && request.resource.data.ownerId == request.auth.uid;
      allow update, delete: if request.auth != null && resource.data.ownerId == request.auth.uid;
    }
  }
}
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

Build a small **Firestore Security Rules Basics** exercise from your current project. First make the smallest working version, then add one accessibility improvement and one failure-state test. Explain out loud what owns the data, what can change it, and what the user sees while it changes.

## Interview-ready answer

**What should a developer remember about Firestore Security Rules Basics?**  
Start with the problem it solves, show the smallest safe implementation, and mention the trade-off. Senior-level answers connect the tool to maintainability, accessibility, performance, security, and the user’s experience—not only API names.
