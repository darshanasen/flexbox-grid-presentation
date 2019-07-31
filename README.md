# Flexbox Grid

Flexbox is a layout method which simplifies the process of styling your content into rows and columns.

___Flexbox Grid___ is a grid system based on the flex display property.

The layout of Flexbox Grid works within a 12 column grid system.

![Gallery image](/images/basic-gallery.png)

Creating the above gallery using Flexbox would probably look like this:

Flexbox HTML
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

Flexbox CSS
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

The first step is to add `class="row"` on the direct flex-parent. Then we add a container around each flex-child with a class signifying its width in columns.


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

Navigate to the [Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid) documentation and add the Grid CSS to our project.

We will be using the CDN:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/flexboxgrid/6.3.1/flexboxgrid.min.css" type="text/css" >
```

Once we've added the Flexbox Grid CDN, replace `class="flex-container"` on the flex parent with `class="row"`.
Then add a container with `class="col-xs-[preferred column width]"` around each flex-child.

You may notice a bit of side-scroll on your test page. If you don't wish to add your own wrapper class, Flexbox Grid has an in-built solution. You can just add a container with a `class="container-fluid"` around any flex-parent.

_Note: The nesting order when setting up Flexbox Grid container classes is _`container-fluid > row > cols`_ _
