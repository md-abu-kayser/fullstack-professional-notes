# Select, Optgroup, and Datalist

select creates a dropdown of option elements, which can be grouped visually with optgroup. datalist is different - it pairs with a regular input to offer autocomplete suggestions the user can still override by typing something else entirely.

```html
<input list="browsers" name="browser">
<datalist id="browsers">
  <option value="Chrome"><option value="Firefox">
</datalist>
```

**Key takeaway:** datalist gives suggestions, not restrictions - select forces a choice from the list.
