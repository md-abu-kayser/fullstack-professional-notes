# Local Storage vs Session Storage vs Cookies

localStorage persists data with no expiration until explicitly cleared, and is shared across all tabs of the same origin. sessionStorage is scoped to a single tab and cleared when that tab closes. Cookies are the only one of the three sent automatically with every HTTP request, which makes them relevant to authentication but also adds overhead to every call.

```javascript
localStorage.setItem("theme", "dark");
sessionStorage.setItem("draftId", "42");
document.cookie = "sessionId=abc123; path=/; Secure";
```

**Key takeaway:** Never store sensitive tokens in localStorage if avoidable - it is fully accessible to any JavaScript running on the page, including from an XSS attack.
