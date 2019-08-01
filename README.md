# Flexbox Grid

Flexbox is a layout method which simplifies the process of styling your content into rows and columns.

___Flexbox Grid___ is a grid system based on the flex display property. It’s essentially a CSS framework which just means it’s a standardized package of CSS code which we can import into our website and use to quickly implement styling.

Similar frameworks/grid systems include [CSS Grids](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) and [Bootstrap](https://getbootstrap.com/).

## What is a grid system and why should we use it?

Grid systems are a layout methodology used by some web designers. Designers are tasked with determining how to visually organize a web page in a coherent and pleasing manner; grid systems are a layout solution which allows designers to arrange and align items within a given format. They are a popular design solution on account of layout consistency and cohesiveness, design and collaboration efficiency and overall user clarity.

## Flexbox Grid implementation

The layout of Flexbox Grid works within a 12-column grid design system. 

![Gallery image](/images/basic-gallery.png)

Creating the above gallery using Flexbox would probably look like this:

Flexbox HTML:
```html
<div class="flex-container">
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
    <div class="gallery-item">
        <img src="images/an-image.png" alt="">
    </div>
</div>
```

Flexbox CSS:
```css
.flex-container {
    display: flex;
    flex-wrap: wrap;
    .gallery-item {
        width: calc(25% - 20px);
        margin: 0 10px;
    }
}
```

If we were to create this gallery using Flexbox Grid, we can achieve the same design simply using HTML.

The first step is to add `class="row"` on the direct flex-parent. Then we add a container around each flex-child with a class signifying its width in columns (`class="col-[viewport-width]-[column-width]"`).


```html
<div class="row">
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
    <div class="col-xs-3">
        <div class="gallery-item">
            <img src="images/an-image.png" alt="">
        </div>
    </div>
</div>
```

In order to test this out, let's start [a new project](/flexbox-grid-test.html).

Let's navigate to the [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid) documentation and add it to our project.

There are a number of ways to include Flexbox Grid within your project but we will be using the CDN:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/flexboxgrid/6.3.1/flexboxgrid.min.css" type="text/css" >
```

Once we've added the Flexbox Grid CDN, replace `class="flex-container"` on the flex parent with `class="row"`.
Then add a container with `class="col-xs-[preferred column width]"` around each flex-child.

You may notice a bit of side-scroll on your test page. If you don't wish to add your own wrapper class, Flexbox Grid has an in-built solution. You can just add a container with `class="container-fluid"` around any flex-parent.

_Note: The nesting order when setting up Flexbox Grid container classes is `container-fluid > row > cols`_

So far we have a basic grid set-up. But what if we wish for our layout to change across viewports?

### Breakpoint classes

* `xs= <48em (Small devices)`
* `sm= >48em (Medium devices)`
* `md= <48em (Large devices)`
* `lg= <48em (Extra-large devices)`

These viewport classes work in ascending order so if you define a column width at `sm` and don't define any other viewports, the styles will be applied from `sm` to `lg`; however, no style will be applied in the `xs` viewport. This is why it's best practice to always start by defining your `xs` viewport styles.

When using breakpoint classes on column widths the setup is `"col-[viewport-width]-[column-width]"`. But with most other classes it's simply `"[styling class]-[viewport-width]"`.

### Alignment classes

`HORIZONTAL`
* `start= flex-start`
* `center= center`
* `end= flex-end`

`VERTICAL`
* `top= flex-start`
* `middle= center`
* `bottom= flex-end`

These classes can be used in conjunction with each other i.e. `class="start-xs top-xs"`

### Distribution classes

If you wish to distribute the contents of a flex-parent or flex-child, the following classes can be used:

* `around= justify-content: space-around`
* `between= justify-content: space-between`

### Re-ordering classes

* `first= order: 0`
* `last`

* `reverse= flex-direction:row-reverse`

### Other classes

![Offset image](/images/grid-offset.png)

If you would like to create space around content within your grid, you can use offset classes to do so. Just ensure that your column and offset numbers always add up to 12 across viewports.

`class="col-xs-offset-4 col-xs-8"`

## Resources
* [Flexbox Grid Classes](http://flexboxgrid.com/)
