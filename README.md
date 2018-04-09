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

#### Flex-box based Grid

Define your column count with the row class.

Create a grid, where each column will reach **3** columns.
```html
<div class="row-3">
    <div class="col"></div>
    <div class="col"></div>
    <div class="col"></div>
</div>
```

Create a grid, where each column will reach **3** columns and on lage screens
it will reach only **2** columns.
```html
<div class="row-3 row-l-2">
    <div class="col"></div>
    <div class="col"></div>
    <div class="col"></div>
</div>
```

But you can define different columns width for each column

```html
<div class="row-3 row-l-2">
    <div class="col-1"></div>
    <div class="col-2"></div>
    <div class="col"></div>
</div>
```

The name defined for your breakpoints will be used for all classes.


### Css Selector

All selector are defined as default, without a breakpoint name

like ```row-6``` or ```order-2```.

#### .row-${breakpoint}-${count}

```row-s-6``` or ```row-6```

#### .col-${breakpoint}-${count}

For the most cases just ```col``` will be sufficent, but when you need
different width you can ```col-d6``` or ```col-s-6```


#### .order-${breakpoint}-${number}
You can change the display order with ```order-2``` or ```order-l-2```.
Its nice to optimize display order for differen breakpoints.


#### .hide-${breakpoint}
You can hide element from 1px to ${breakpoint} size.

```hide-s``` will hide you element until the next bigger breakpoint is reached, this will be ```m```

The opposit functionality is:

#### .show-${breakpoint}

Hide element from 1px until the breakpoint is reached.


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



