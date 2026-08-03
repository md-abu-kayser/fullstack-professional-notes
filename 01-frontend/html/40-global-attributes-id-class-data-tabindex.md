# Global Attributes: id, class, data-*, tabindex

Global attributes work on virtually any HTML element. id uniquely identifies one element per page; class groups elements for styling or scripting; data-* attributes store custom data without inventing new HTML; tabindex controls keyboard focus order.

```html
<div id="cart" class="widget" data-item-count="3" tabindex="0"></div>
```

**Key takeaway:** Avoid positive tabindex values - they override natural document order and confuse keyboard navigation.
