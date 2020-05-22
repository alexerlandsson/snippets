# Footer always at bottom

Trick to always place the footer at the bottom of the viewport, even if the content is shorter than the viewport itself.

## HTML

```html
<body>
  <main>
    <!-- Page content... -->
  </main>
  <footer>
    <!-- Footer content -->
  </footer>
</body>
```

## CSS

```css
html,
body {
  min-height: 100%;
  min-height: -webkit-fill-available;
}

body {
  display: flex;
  flex-direction: column;
}

main {
  flex: 1 1 auto;
}

footer {
  margin-top: auto;
}
```
