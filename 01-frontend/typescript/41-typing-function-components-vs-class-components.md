# Typing Function Components vs Class Components

Function components are typically typed by simply typing their props parameter directly - the once-common React.FC type is now generally discouraged since it implicitly adds a children prop and complicates generic components. Class components type both props and state via generic type parameters on Component.

```tsx
// Preferred modern style
function Card({ title }: { title: string }) { return <div>{title}</div>; }

// Class component typing
class Counter extends React.Component<{ start: number }, { count: number }> {
  state = { count: this.props.start };
}
```

**Key takeaway:** Most teams have moved away from React.FC in favor of typing the props parameter directly - it is more explicit and plays better with generics.
