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
  overscroll-behavior: contain;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
}

.item {
  scroll-snap-align: center;
}
```
