# Vertically align to first row of text

Align an icon or checkbox etc. vertically to the first row of text placed next to it.

## SCSS

```scss
$iconSize: 20px;
$fontSize: 1rem;
$lineHeight: 1.5;

.icon {
  margin-top: calc(($iconSize - $fontSize * $lineHeight) / -2);
}
```

## Component example

### HTML

```html
<div class="foo">
  <div class="foo__icon">[ICON]</div>
  <div class="foo__text">Lorem ipsum dolor sit amet</div>
</div>
```

### SCSS

```scss
$iconSize: 20px;
$fontSize: 1rem;
$lineHeight: 1.5;

.foo {
  display: flex;

  &__icon {
    flex-shrink: 0;
    width: $iconSize;
    height: $iconSize;
    margin-top: calc(($iconSize - $fontSize * $lineHeight) / -2);
    margin-right: 16px;
  }

  &__text {
    flex: 1 1 auto;
    font-size: $iconSize;
    line-height: $lineHeight;
  }
}
```
