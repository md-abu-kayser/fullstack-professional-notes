# next.config.js Key Options

next.config.js customizes build and runtime behavior: images.domains (or remotePatterns) whitelists external image hosts for next/image, redirects and rewrites define URL rules, and env can expose additional build-time variables beyond the NEXT_PUBLIC_ convention.

```javascript
module.exports = {
  images: { remotePatterns: [{ hostname: "cdn.example.com" }] },
  async redirects() {
    return [{ source: "/old-page", destination: "/new-page", permanent: true }];
  },
};
```

**Key takeaway:** next/image will refuse to load external images from a host not explicitly whitelisted in remotePatterns - a common source of "image not showing" issues after adding a new image source.
