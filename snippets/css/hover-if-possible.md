# :hover if possible

CSS used to add :hover to an element if it is possible. The :hover will only be available on devices using pointer devices and not on touch based devices.

## CSS

```css
@media (any-hover: hover) and (any-pointer: fine) {
  .element:hover {
    /* Hover properties */
  }
}
```

## SCSS

```scss
.element {
  @media (any-hover: hover) and (any-pointer: fine) {
    &:hover {
      /* Hover properties */
    }
  }
}
```
