# Flexbox Grid

Flexbox is a layout method which simplifies the process of styling your content into rows and columns.

___Flexbox Grid___ is a grid system based on the flex display property.

The layout of Flexbox Grid works within a 12 column grid system.

![Gallery image](/images/basic-gallery.png)

A gallery using Flexbox would probably look like this:

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

If we were to create this gallery using Flexbox Grid, we can do it simply using HTML.

The first step is to add `class="row"` on the direct parent element. Followed by a container with a class signifying the amount of columns the flex-child takes up.


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

[Flexbox Grid](https://github.com/kristoferjoseph/flexboxgrid)
