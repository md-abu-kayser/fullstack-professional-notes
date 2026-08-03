# CSS Architecture: BEM Methodology

BEM (Block, Element, Modifier) is a naming convention that keeps class names self-documenting and collision-resistant: block is the standalone component, element is a part of that block (block__element), and modifier is a variation (block--modifier). It scales well in large codebases without a build tool.

```css
.card { }
.card__title { }
.card--featured { }
```

**Key takeaway:** BEM's biggest win is eliminating specificity wars - every selector is a single flat class, so nothing ever needs to fight for precedence.
