# Select siblings between

Selector used to select siblings between to selectable elements. Source: [Bramus](https://www.bram.us/2023/01/12/sibling-scopes-in-css-thanks-to-has).

## HTML

```html
<ul>
  <li>outside</li>
  <li class="from">from</li>
  <li>in-between</li>
  <li>in-between</li>
  <li>in-between</li>
  <li>in-between</li>
  <li class="to">to</li>
  <li>outside</li>
</ul>
```

## CSS

```css
.from ~ :has(~ .to) {
  outline: 1px solid red;
}
```
