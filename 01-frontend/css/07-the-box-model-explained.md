# The Box Model Explained

Every element is a rectangular box made of four layers, from inside out: content, padding, border, and margin. The total visible size of an element is the sum of all four - a fact that trips up beginners constantly when elements do not line up as expected.

```css
.box {
  width: 200px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
/* Total rendered width (default box-sizing): 200 + 40 + 4 = 244px */
```

**Key takeaway:** This is exactly why box-sizing: border-box exists - it makes width include padding and border, matching what most developers intuitively expect.
