# Magnific Popup

- https://dimsemenov.com/plugins/magnific-popup/


## Documentation

- https://dimsemenov.com/plugins/magnific-popup/documentation.html


## Html Markup

```html

<!-- image popup -->
<a class="popup-image" href="{image-src}">
	<img src="{image-src}">
</a>

<!-- video popup -->
<a class="popup-video" href="{video-src}">
	<i class="fa fa-play"></i>
</a>

```

## Js Code

```js

/* magnificPopup img view */
$('.popup-image').magnificPopup({
	type: 'image',
	gallery: {
	  enabled: true
	}
});

/* magnificPopup video view */
$('.popup-video').magnificPopup({
	type: 'iframe'
});


```
