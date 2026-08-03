# Migrating a JavaScript Project to TypeScript

A practical migration path: add a tsconfig.json with allowJs and checkJs enabled first to get type checking on existing .js files without renaming anything, then rename files to .ts incrementally, starting with leaf utility modules that have few dependencies, working strict mode up gradually rather than all at once.

```json
{ "compilerOptions": { "allowJs": true, "checkJs": true, "strict": false } }
```

**Key takeaway:** Migrating incrementally, file by file, with strict mode off initially and tightened over time, is far more sustainable than attempting a single big-bang rewrite of an entire codebase.
