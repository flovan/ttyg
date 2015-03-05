![TTYG](https://raw.github.com/flovan/ttyg/master/ttyg.gif)

#Talk To Your Grid v0.1

TTYG is an attempt at creating a smart SCSS grid mixin that understand human language, while at the same time outputting DRY code.

For optimal results, this mixin should be used in combination with CSS3 level selectors, as well as a [CSS minifier](https://www.npmjs.com/package/clean-css) and/or [mixin merger](https://www.npmjs.com/package/group-css-media-queries).

[&rarr; Demo page &larr;](http://flovan.me/ttyg)

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

## TODO

* Add more complex scenarios, and write some kind of automated test to check all of the output.
* Add `no-gutter` option somewhere.
* Add regular classes into stylesheet in `_classes.scss`
* DRY out mixin code
* Fix offsets that cause horizontal scrollbar (eg `@warn` when offset + col > context, and override below min-breakpoint)
* Testing!

## Credits

This mixin was developed and tested on [Sassmeister](http://sassmeister.com), a great tool that allows you to live-test Sass with both Libsass and Rubysass, and saves everything to a Github Gist.

A big thanks to [Hugo Giraudel](http://hugogiraudel.com), as well as to [the @import team](https://github.com/at-import). I borrowed quite a few of your helper functions for this one!

[Gif source](http://kidmograph.tumblr.com/post/83623951490/lght)