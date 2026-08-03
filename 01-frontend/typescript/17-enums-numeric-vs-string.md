# Enums: Numeric vs String

Numeric enums auto-assign increasing integer values starting from 0 unless specified. String enums require an explicit string value for every member, and are generally preferred since their runtime values are self-descriptive in logs and debugging rather than opaque numbers.

```typescript
enum Status {
  Pending = "PENDING",
  Active = "ACTIVE",
  Banned = "BANNED",
}
```

**Key takeaway:** String enums are usually the safer default - a stray numeric enum value logged or serialized is much harder to debug than a readable string.
