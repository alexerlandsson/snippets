# Keyboard only :focus

Adds styling when elements is focues with a keyboard and not a mouse in supported browsers.

## SCSS

```scss
@use "sass:string";

@mixin focus($selector-focus-visible: ":focus-visible", $selector-focus: ":focus") {
  @supports selector(:focus-visible) {
    &#{string.unquote($selector-focus-visible)} {
      @content;
    }
  }

  // Safari & IE11
  @supports not selector(:focus-visible) {
    &#{string.unquote($selector-focus)} {
      @content;
    }
  }
}

:where(a, button, input, select, textarea, summary, [role="button"]) {
  --focus-outline-size: max(2px, 0.08em);
  --focus-outline-style: solid;
  --focus-outline-color: #2162ec;

  @include focus {
    outline: var(--focus-outline-size) var(--focus-outline-style) var(--focus-outline-color);
    outline-offset: var(--focus-outline-offset, var(--focus-outline-size));
  }
}
```
