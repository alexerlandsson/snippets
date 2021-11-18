# CSS Focus

Reset default UA focus and replace it with custom focus styling using `:focus-visible` with `:focus` fallback for unsupported browsers.

## SCSS

```scss
@mixin focus {
  @supports selector(:focus-visible) {
    &:focus-visible {
      @content;
    }
  }

  @supports not selector(:focus-visible) {
    &:focus {
      @content;
    }
  }
}

// Remove inner focus on buttons in Firefox
::-moz-focus-inner {
  border: none;
}

// Remove default focus outline
:focus {
  outline: none;
}

// Add custom default focus to focusable elements
a,
button,
input,
select,
textarea {
  @include focus {
    outline: 2px solid #2162ec;
  }
}
```
