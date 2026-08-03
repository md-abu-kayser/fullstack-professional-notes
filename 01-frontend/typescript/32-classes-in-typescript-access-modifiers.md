# Classes in TypeScript: Access Modifiers

public (the default) properties are accessible from anywhere. private restricts access to within the declaring class only, not even subclasses. protected allows access within the class and its subclasses, but not from outside instances.

```typescript
class BankAccount {
  private balance: number = 0;
  protected accountId: string = crypto.randomUUID();
  deposit(amount: number) { this.balance += amount; }
}
```

**Key takeaway:** These access modifiers are enforced only at compile time - like other TypeScript features, they produce no actual runtime privacy protection in the compiled JavaScript.
