# Route Groups and Parallel Routes

Route groups (folder names in parentheses) organize routes or apply a shared layout without adding a segment to the URL. Parallel routes (folder names with an @ prefix) render multiple independent pages into named slots of the same layout simultaneously, like a dashboard with independent panels.

```
app/(marketing)/about/page.tsx   -> /about, no "marketing" in the URL
app/@modal/page.tsx               -> rendered into a named "modal" slot
```

**Key takeaway:** Route groups solve organizational and layout-sharing needs; parallel routes solve rendering genuinely independent UI regions side by side - they address different problems despite similar-looking syntax.
