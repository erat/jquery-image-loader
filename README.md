# jQuery image loader

Load images asynchronously with ease. This plugin seeks for all images with data-src attributes inside a wrapper or run the plugin on an image tag itself.

The data-src attribute will be copied to the src attribute, which gives you enough feedback to get a good grip on the situation.

## Callbacks

* imgLoadedClb - Triggered when an image is loaded. ('this' is the loaded image
* allLoadedClb - Triggered when all images are loaded. ('this' is the wrapper in which all images are loaded, or the image if you ran it on one image)
* imgErrorClb - Triggered when the image gives an error. Useful when you want to add a placeholder instead or remove it. ('this' is the loaded image)
* noImgClb - Triggered when there are no image found with data-src attributes, or when all images give an error. ('this' is the wrapper in which all images are loaded, or the image if you ran it on one image)
* dataAttr - The data attribute that contains the source. (Default: 'src')

## How to use?

### HTML

```html
<div class="images">
  <img data-src="link-to-image.jpg" alt="">
  <img data-src="link-to-image.jpg" alt="">
  <img data-src="link-to-image.jpg" alt="">
</div>
```

### Javascript to load images inside a wrapper

```javascript
$('.images').loadImages({
  imgLoadedClb: function(){},
  allLoadedClb: function(){},
  imgErrorClb:  function(){},
  noImgClb:     function(){},
  dataAttr:     'src'
});
```

### Javascript to load one image

```javascript
$('.images img').first().loadImages({
  imgLoadedClb: function(){},
  allLoadedClb: function(){},
  imgErrorClb:  function(){},
  noImgClb:     function(){},
  dataAttr:     'src'
});
```

## Demo time!
[http://mrhenry.github.com/jquery-image-loader/public/](http://mrhenry.github.com/jquery-image-loader/public/)
