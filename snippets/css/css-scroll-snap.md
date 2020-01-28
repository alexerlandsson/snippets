# CSS Scroll Snap

Easiest way to create an overflow scroll with scroll snap.

## HTML

```html
<div class="container">
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
  <div class="item"></div>
</div>
```

## CSS

```css
.container {
  overflow: auto;
  -webkit-overflow-scrolling: touch;
  scroll-snap-type: x mandatory;

  /* This will prevent default page scroll */
  overscroll-behavior: contain;
}

.item {
  scroll-snap-align: center;
}
```
