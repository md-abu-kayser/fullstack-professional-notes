# Typing React Props and State

React component props are typed with an interface or type alias describing exactly what a component accepts, catching missing or mistyped props at compile time instead of at runtime. useState can be given an explicit generic when the initial value does not fully convey the intended type.

```tsx
interface ButtonProps {
  label: string;
  onClick: () => void;
  variant?: "primary" | "secondary";
}

function Button({ label, onClick, variant = "primary" }: ButtonProps) {
  return <button onClick={onClick} className={variant}>{label}</button>;
}
```

**Key takeaway:** Typing props explicitly turns "forgot to pass a required prop" from a runtime bug into an immediate red squiggle in the editor.
