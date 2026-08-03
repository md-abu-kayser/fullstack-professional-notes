# Typing Custom Hooks

A custom hook's return type is inferred automatically from what it returns, but explicitly typing complex return values (especially tuples, similar to useState's own [value, setValue] pattern) improves clarity and autocomplete for anyone consuming the hook.

```typescript
function useToggle(initial = false): [boolean, () => void] {
  const [value, setValue] = useState(initial);
  const toggle = () => setValue(v => !v);
  return [value, toggle];
}
```

**Key takeaway:** Explicitly annotating a tuple return type prevents TypeScript from widening it to a plain array, which would lose the fixed order and types of each element.
