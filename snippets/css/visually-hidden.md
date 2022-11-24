# Visually hidden

Snippet used to visually hide elements and only make them accessible through screen readers.

## CSS

```css
.sr-only {
  &:not(:focus) {
    position: absolute;
    width: 1px;
    height: 1px;
    clip-path: inset(50%);
    overflow: hidden;
    white-space: nowrap;
  }
}
```

## Sources
* [The anatomy of visually-hidden](https://www.tpgi.com/the-anatomy-of-visually-hidden/) by James Edwards
