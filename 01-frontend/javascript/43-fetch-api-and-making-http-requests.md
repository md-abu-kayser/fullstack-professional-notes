# Fetch API and Making HTTP Requests

fetch is the modern, promise-based API for making HTTP requests, replacing the older XMLHttpRequest. It resolves as soon as headers are received - even for a 404 or 500 response - so checking response.ok is necessary to detect HTTP-level errors, which fetch does not reject on by default.

```javascript
async function getUser(id) {
  const response = await fetch(`/api/users/${id}`);
  if (!response.ok) throw new Error(`HTTP ${response.status}`);
  return response.json();
}
```

**Key takeaway:** fetch only rejects on network failure, not on HTTP error status codes - always check response.ok explicitly.
