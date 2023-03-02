# Inner rounded corners

Use this trick to create visually pleasing rounded corners on an inner element.

## CSS

```css
.rounded {
  --r: 16px;
  --p: 8px;

  padding: var(--p);
  border-radius: calc(var(--r) + var(--p));

  &__inner {
    border-radius: var(--r);
  }
}
```

## HTML

```html
<div class="rounded">
  <div class="rounded__inner"></div>
</div>
```
