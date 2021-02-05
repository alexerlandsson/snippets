# Picture

Basic html picture markup.

## HTML

To support IE11, use a reasonable big image as fallback image in the src element.

### Art Direction

Adding `media=""` to the image lets you use different images or formats in different breakpoints.

```html
<picture>
  <source media="(min-width: 767px)" srcset="path_to_image/image?w=767&h=400">
  <source media="(min-width: 500px)" srcset="path_to_image/image?w=500&h=400">
  <img src="path_to_image/image?w=375&h=375" alt="" />
</picture>
```

### Performance

Change resolution on an image depending on browser width. This method could also be used to add different media formats such as webp. Browsers without webp support will fallback to a format it does support.

```html
<picture>
  <source
    type="image/webp"
    srcset="path_to_image/image?w=600&format=webp 600w,
            path_to_image/image?w=900&format=webp 900w,
            path_to_image/image?w=1200&format=webp 1200w"
    sizes="(min-width: 1400px) 1300px, calc(100vw - 32px)"
  >
  <img
    srcset="path_to_image/image?w=600 600w,
            path_to_image/image?w=900 900w,
            path_to_image/image?w=1200 1200w"
    sizes="(min-width: 1400px) 1300px, calc(100vw - 32px)"
    src="path_to_image/image?w=1200"
    alt=""
  />
</picture>
```
