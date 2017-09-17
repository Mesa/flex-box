# flex-box

A very simple and small flex-box grid system, with some helper mixins.


include this scss file into your own project assets.

```scss
@import "flex-box/main.scss";
```

Define your breakpoints before you include the main scss file.

```scss
$grid-columns: 12;

$micro:  'x';
$small:  's';
$medium: 'm';
$large:  'l';

$grid-breakpoints: (
   $micro: 1px,
   $small: 600px,
   $medium: 800px,
   $large: 1000px
) ;
```

Generate your assets with Grunt, Webpack or what is currently the hottes "must have" 
Javascript scss preprocessor.


#### Media queries

```scss
@include media($micro) {
    padding-left:  .5rem;
    padding-right: .5rem;
}
```

Now you can include the "media" mixin and when you change your breakpoint,
all media queries change too.

My biggest benefit is, that i don't have to remember the hole media query und can use my own ;).


To be continued...