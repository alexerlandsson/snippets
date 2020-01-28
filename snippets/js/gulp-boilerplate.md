# Gulp boilerplate

Boilerplate for a basic gulp installation.

## Terminal

To install gulp and selected dependencies, run the following commands from terminal.

```bash
npm init
```

```bash
npm install --save-dev gulp gulp-sass gulp-rename gulp-clean-css
```

## JavaScript

Create a file called `gulpfile.js` with the following code.

```js
var gulp = require('gulp');
var sass = require('gulp-sass');
var rename = require('gulp-rename');
var minifycss = require('gulp-clean-css');
var replace = require('gulp-replace');

var paths = {
  sass: {
    src: './src/style/*.scss',
    dest: './dist/style',
    watch: './src/style/**/*.scss'
  },
  html: {
    src: './src/index.html',
    dest: './dist'
  },
  images: {
    src: './src/assets/images/**/*',
    dest: './dist/assets/images'
  },
};

// CSS
gulp.task('sass', function() {
  return gulp
    .src(paths.sass.src)
    .pipe(sass())
    .pipe(rename({suffix: '.min'}))
    .pipe(minifycss())
    .pipe(gulp.dest(paths.sass.dest));
});

// HTML
gulp.task('html', function() {
  return gulp
    .src(paths.html.src)
    .pipe(gulp.dest(paths.html.dest));
});

// Images
gulp.task('images', function() {
  return gulp
    .src(paths.images.src)
    .pipe(gulp.dest(paths.images.dest));
});

// Watch
gulp.task('watch', function() {
  gulp.watch(paths.sass.watch, gulp.series('sass'));
  gulp.watch(paths.html.src, gulp.series('html'));
});

// Default
gulp.task('default', gulp.series('sass', 'html', 'images'));
```
