# Image reset

Basic img reset CSS based on Harry Roberts Twitter post (https://twitter.com/csswizardry/status/1717841334462005661).

## CSS

```css
img {
  max-width: 100%; /* [1] */
  height: auto; /* [1] */
  vertical-align: middle; /* [2] */
  font-style: italic; /* [3] */
  background-repeat: no-repeat; /* [4] */
  background-size: cover; /* [4] */
  shape-margin: 0.75rem; /* [5] */
}

/*
  1. Allow for fluid image sizing while maintaining aspect ratio governed by width/height attributes
  2. Remove ‘phantom’ whitespace
  3. Italicise alt text to visually offset it from surrounding copy
  4. [Inert] Set up backgrounds for optional LQIP
  5. [Inert] Set up margin for optional `shape-outside`
*/
```
