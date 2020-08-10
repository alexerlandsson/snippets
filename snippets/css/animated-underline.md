# Animated underline

Technique to animate underline to text.

## CSS

```css
a {
  color: #000;
  text-decoration: none;
  background-image: linear-gradient(#000, #000), linear-gradient(#0000ff, #0000ff);
  background-size: 100% 2px, 0 2px; /* 2px is the height of the underline */
  background-position: 100% 100%, 0 100%;
  background-repeat: no-repeat;
  transition: background-size 300ms linear;
}

a:hover {
  background-size: 0 2px, 100% 2px;
}
```
