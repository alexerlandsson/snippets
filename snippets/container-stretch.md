# Container stretch

Simple way to give an element 100% viewport width even when placed inside a container with a defined width.

## HTML

```html
<div class="container">
  <div class="stretch">
    This div ignores the width of .container
  </div>
</div>
```

## CSS

```css
.container {
  width: 100%;
	max-width: 800px;
	margin: 0 auto;
  padding: 0 32px;
}

.stretch {
	position: relative;
  width: 100vw;
	left: 50%;
	right: 50%;
	margin-left: -50vw;
	margin-right: -50vw;
}
```
