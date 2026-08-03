# Print Stylesheets

A @media print block lets you define styles that apply only when a page is printed or exported to PDF - hiding navigation and ads, forcing black text on white background, and adding visible URLs after links for reference.

```css
@media print {
  nav, footer, .no-print { display: none; }
  body { color: #000; background: #fff; }
  a::after { content: " (" attr(href) ")"; }
}
```

**Key takeaway:** Print stylesheets are easy to forget entirely, but a few lines can massively improve the experience for anyone who prints a page or invoice.
