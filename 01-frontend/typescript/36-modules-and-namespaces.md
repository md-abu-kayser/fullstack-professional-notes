# Modules and Namespaces

Modern TypeScript projects use standard ES modules (import/export) for code organization across files. The older namespace keyword predates ES modules and groups related code under a single global-like identifier - largely legacy today, seen mostly in older codebases or .d.ts files for global libraries.

```typescript
// modern, preferred
export interface User { id: string; }

// legacy namespace pattern - rarely needed in new code
namespace Utils {
  export function formatDate(date: Date) { /* ... */ }
}
```

**Key takeaway:** Default to ES modules for all new TypeScript code - namespaces are essentially a legacy pattern kept for backward compatibility.
