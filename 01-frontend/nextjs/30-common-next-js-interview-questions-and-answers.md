# Common Next.js Interview Questions and Answers

Frequent topics include: explaining Server versus Client Components and why the split matters for bundle size, the differences between SSG, SSR, and ISR, how the App Router's file conventions (layout, loading, error) work, and when you would choose a Server Action over a traditional API route.

```jsx
// Be ready to explain why this ships zero JS for itself:
export default async function Page() {
  const data = await getData();
  return <List data={data} />;
}
```

**Key takeaway:** Interviewers often care most about whether you understand why Server Components exist (less client JavaScript, direct data access) rather than just their syntax.
