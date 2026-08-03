# Error Objects and Custom Errors

The built-in Error object carries a message and stack trace. Extending it lets you create custom error types (like ValidationError or NotFoundError) that carry additional context and can be distinguished with instanceof in catch blocks, enabling different handling per error type.

```javascript
class ValidationError extends Error {
  constructor(message, field) {
    super(message);
    this.name = "ValidationError";
    this.field = field;
  }
}
```

**Key takeaway:** Always set this.name in a custom error class - otherwise it reports as "Error" in logs and stack traces, hiding what actually went wrong.
