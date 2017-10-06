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
