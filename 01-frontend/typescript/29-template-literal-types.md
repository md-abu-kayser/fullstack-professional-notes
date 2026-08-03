# Template Literal Types

Template literal types build new string literal types by combining other literal types with static text, using the same backtick syntax as JavaScript template literals but evaluated entirely at the type level.

```typescript
type EventName = "click" | "focus" | "blur";
type HandlerName = `on${Capitalize<EventName>}`; // "onClick" | "onFocus" | "onBlur"
```

**Key takeaway:** Combined with Capitalize/Uncapitalize/Uppercase/Lowercase, template literal types can auto-generate whole families of related string literal types from one source union.
