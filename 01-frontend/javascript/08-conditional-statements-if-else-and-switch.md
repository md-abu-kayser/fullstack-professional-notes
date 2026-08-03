# Conditional Statements: if-else and switch

if-else evaluates arbitrary boolean expressions and is best for a small number of distinct conditions. switch compares one value against multiple exact matches and is often clearer when checking many possible values of the same variable - just remember break to avoid fallthrough.

```javascript
switch (role) {
  case "admin":
    grantFullAccess();
    break;
  case "editor":
    grantEditAccess();
    break;
  default:
    grantViewAccess();
}
```

**Key takeaway:** Forgetting break in a switch case is one of the most common JavaScript bugs - execution silently falls through into the next case.
