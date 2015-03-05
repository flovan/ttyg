<<<<<<< HEAD
Nothing to see here, move along..
=======
![TTYG](https://raw.github.com/flovan/ttyg/master/ttyg.gif)

#Talk To Your Grid v0.1

TTYG is an attempt at creating a smart SCSS grid mixin that understands human language.

Columns are on-demand, so no CSS is compiled until you ask for it through an `@include` command. Output is made DRY as possible, but it is advised to combine this mixin with a [CSS minifier](https://www.npmjs.com/package/clean-css) and/or [mixin merger](https://www.npmjs.com/package/group-css-media-queries).

[&rarr; Documentation and Demos &larr;](http://flovan.me/ttyg)

## Example usage

````sass
.test-single-part {
  @include col(4);
}
.test-edge {
  @include col(4 edge);
}
.test-centered {
  @include col(5 centered);
}
.test-no-break {
  @include col(6 no-break);
}
.test-offset {
  @include col(4 offset 8);
}
.test-push {
  @include col(6 push 6);
}
.test-pull {
  @include col(6 pull 6);
}
.test-of {
  @include col(4 of 16);
}
.test-from {
  @include col(6 from 1000px);
}
.test-to {
  @include col(6 to 1000px);
}
.test-from-to {
  @include col(6 from 1000px to 1200px);
}
.test-from-to-then {
  @include col(6 from 1000px to 1200px then 3);
}
.test-to-then {
  @include col(6 to 1000px then 3);
}
.test-from-to-multi-then {
  @include col(6 from 1000px to 1200px then 3 to 1400px then 4);
}
````

[Gif source](http://kidmograph.tumblr.com/post/83623951490/lght)
>>>>>>> dev
