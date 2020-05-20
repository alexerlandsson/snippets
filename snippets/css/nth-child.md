# :nth-child

Quick guide for common :nth-child selectors.

## Select only the fifth element

```css
.element:nth-child(5) {
  /* Styling... */
}
```

## Select all but the first five

```css
.element:nth-child(n+6) {
  /* Styling... */
}
```

## Select only the first five

```css
.element:nth-child(-n+5) {
  /* Styling... */
}
```

## Select every fourth, starting at the first

```css
.element:nth-child(4n+1) {
  /* Styling... */
}
```

## Select only odd

```css
.element:nth-child(odd) {
  /* Styling... */
}
```

## Select only even

```css
.element:nth-child(even) {
  /* Styling... */
}
```

## Select the second to last element

```css
.element:nth-last-child(2) {
  /* Styling... */
}
```
