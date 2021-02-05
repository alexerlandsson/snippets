# Retina image

Use `srcset` to add an image used on a high resolution display.

## HTML

```html
  <img src="path_to_image/image?w=100" srcset="path_to_image/image?w=200 2x" alt="" />
```

### Webp

Use in combination with a `<picture>` element to add webp images to supported browsers.

```html
  <picture>
    <source
      type="image/webp"
      srcset="path_to_image/image?w=100&format=webp,
              path_to_image/image?w=200&format=webp 2x"
    />
    <img src="path_to_image/image?w=100" srcset="path_to_image/image?w=200 2x" alt="" />
  </picture>
```
