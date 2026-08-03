# Image Optimization with next/image

The Image component automatically serves correctly sized, modern-format images, lazy-loads by default, and prevents layout shift by requiring width and height (or using fill) upfront - all without manual srcset or picture element work.

```jsx
import Image from "next/image";

<Image src="/hero.jpg" alt="Hero banner" width={1200} height={600} priority />
```

**Key takeaway:** Use the priority prop only for the single most important above-the-fold image (like a hero image) - overusing it defeats the lazy-loading benefit for everything else.
