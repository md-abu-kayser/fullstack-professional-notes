# Fieldset and Legend

fieldset groups related form controls (like a set of radio buttons) into a single semantic unit, and legend gives that group a title. Screen readers announce the legend before each control inside, avoiding repetitive labeling.

```html
<fieldset>
  <legend>Preferred contact method</legend>
  <input type="radio" name="contact" id="email-opt"><label for="email-opt">Email</label>
  <input type="radio" name="contact" id="phone-opt"><label for="phone-opt">Phone</label>
</fieldset>
```

**Key takeaway:** fieldset and legend matter most for radio or checkbox groups where individual labels alone lack context.
