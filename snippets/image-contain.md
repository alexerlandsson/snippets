# Image contain

Contain an image inside a container of either an absolute or relative size.

## HTML

```html
<div class="container">
  <img src="" alt="" class="img" />
</div>
```

## CSS

```css
.container {
  position: relative;
  width: 400px;
  height: 300px;
}

.img {
  display: block;
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  max-width: 100%;
  max-height: 100%;
}
```
