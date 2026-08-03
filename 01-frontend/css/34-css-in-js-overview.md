# CSS-in-JS Overview

CSS-in-JS libraries let you write styles directly inside JavaScript/TypeScript component files, often with access to props and theme variables at style-definition time. This colocates styling with logic but historically added a runtime cost, which is why many newer tools compile styles at build time instead.

```jsx
const Button = styled.button`
  padding: 8px 16px;
  background: ${props => props.primary ? "blue" : "gray"};
`;
```

**Key takeaway:** Runtime CSS-in-JS can add measurable bundle size and render cost - check whether a project's chosen library compiles at build time instead.
