# tsconfig.json Key Options

tsconfig.json configures how the compiler behaves. strict enables a bundle of safety checks together (recommended for all new projects). target sets which JavaScript version is emitted. module and moduleResolution control how imports are resolved and compiled.

```json
{
  "compilerOptions": {
    "strict": true,
    "target": "ES2020",
    "module": "ESNext",
    "moduleResolution": "bundler"
  }
}
```

**Key takeaway:** Enabling strict from the very start of a project is far easier than retrofitting it onto a large, already-loosely-typed codebase later.
