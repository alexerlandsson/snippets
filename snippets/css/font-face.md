# Font Face

Boilerplate on how to load local fonts using `@font-face` focusing on performance.

## CSS

There are two important things when loading fonts using `@font-face` - load `woff2` before `woff` (if available) and make sure `font-display: swap;` is added.

```css
@font-face {
  font-family: 'Font Name';
  src:  url('/PATH_TO_FONT/FILE_NAME.woff2') format('woff2'),
        url('/PATH_TO_FONT/FILE_NAME.woff') format('woff');
  font-weight: 400;
  font-style: normal;
  font-stretch: normal;
  font-display: swap;
}
```

When using `font-display: swap;` it is important to have a fallback font which is similar to the imported one since the font will be swapped and cause a flash in the layout.

```css
body {
  font-family: 'Font Name', FALLBACK_FONT, sans-serif;
}
```

## HTML

Add this snippet to the HTML `<head>` in order to preload the local font.

```html
<link rel="preload" href="/PATH_TO_FONT/FILE_NAME.woff2" as="font" type="font/woff2" crossorigin>
```
