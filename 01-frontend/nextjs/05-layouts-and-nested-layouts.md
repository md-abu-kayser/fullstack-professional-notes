# Layouts and Nested Layouts

A layout.tsx wraps every page within its folder and persists across navigations between those pages - it does not re-render or lose its state, which is ideal for things like a sidebar or a persistent audio player. Layouts nest naturally: a child folder's layout renders inside its parent's.

```jsx
// app/dashboard/layout.tsx
export default function DashboardLayout({ children }) {
  return (
    <div className="dashboard">
      <Sidebar />
      <main>{children}</main>
    </div>
  );
}
```

**Key takeaway:** Because layouts persist across navigation, they are the right place for state that should survive moving between sibling pages, like an open sidebar or scroll position.
