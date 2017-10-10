# SCSS NOTES
Note for SCSS

### Variable
SCSS
```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
After compile
```
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}
```

### Mixins
SCSS
```
$breakpoint-sp: 768px;
@mixin min-screen($breakpoint-sp) {
  @media screen and (min-width: #{$breakpoint-sp + 1px}) {
    @content;
  }
}

.l-header {
  @include min-screen($breakpoint-sp) {
    # Add style here
  }
}
```
After compile
```
@media screen and (min-width: 769px) {
  .l-header {
    background-image: url("/imgs/header.png");
    background-size: 100%;
    background-repeat: no-repeat; 
  } 
}
```
