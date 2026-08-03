# Form Handling with Server Actions

Passing a Server Action directly to a form's action prop lets the form submit and mutate data without any client-side JavaScript or manual fetch call, while still supporting progressive enhancement - the form works even before hydration finishes.

```jsx
export default function NewPostForm() {
  return (
    <form action={createPost}>
      <input name="title" />
      <button type="submit">Create</button>
    </form>
  );
}
```

**Key takeaway:** Because Server Action forms degrade gracefully, they keep working even if JavaScript fails to load - a meaningful resilience win over purely client-side form handling.
