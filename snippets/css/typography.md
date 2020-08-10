# Typography

Basic technics to improve the legibility.

## CSS

### Make different fonts the same size

`font-size-adjust` will adjust the height of lowercase "x" relative to the font-size.

```scss
article {
  @supports (font-size-adjust: 1) {
    font-size-adjust: 0.5;
  }
}
```

### Generic margins and line-height

Calculations for line-height and margin are based on [this article](https://www.smashingmagazine.com/2020/07/css-techniques-legibility/?utm_source=CSS-Weekly&utm_campaign=Issue-421&utm_medium=email).

```scss
article {
  > * {
    &:first-child {
      margin-top: 0;
    }

    &:last-child {
      margin-bottom: 0;
    }
  }

  h1 {
    font-size: 2.5em;
    line-height: calc(1ex / 0.42);
    margin: calc(1ex / 0.42) 0;
  }

  h2 {
    font-size: 2em;
    line-height: calc(1ex / 0.42);
    margin: calc(1ex / 0.42) 0;
  }

  h3 {
    font-size: 1.75em;
    line-height: calc(1ex / 0.38);
    margin: calc(1ex / 0.38) 0;
  }

  h4 {
    font-size: 1.5em;
    line-height: calc(1ex / 0.37);
    margin: calc(1ex / 0.37) 0;
  }

  p {
    font-size: 1em;
    line-height: calc(1ex / 0.32);
    margin: calc(1ex / 0.32) 0;
  }
}
```
