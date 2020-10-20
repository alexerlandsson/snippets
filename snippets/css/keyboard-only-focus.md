# Keyboard only :focus

Adds styling when elements is focues with a keyboard and not a mouse.

## CSS

```css
/* Adds custom focus styling to specific elements */
.element:focus-visible {
  outline: 2px dashed #000;
}
  
/* Removes outline from mouse focus */
*:focus:not(:focus-visible) {
  outline: none;
}
```
