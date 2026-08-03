# Font Optimization with next/font

next/font automatically self-hosts fonts (including Google Fonts) at build time, eliminating extra network requests to a third-party font CDN and avoiding layout shift from font-swapping, while keeping the simple API of just importing and applying a font.

```jsx
import { Inter } from "next/font/google";
const inter = Inter({ subsets: ["latin"] });

export default function RootLayout({ children }) {
  return <html className={inter.className}>{children}</html>;
}
```

**Key takeaway:** Because fonts are self-hosted at build time, there is no runtime request to Google's servers at all - a real privacy and performance improvement over a plain link tag.
