# Slick Slider

- http://kenwheeler.github.io/slick/


## Dependencies

- [slick](https://github.com/kenwheeler/slick/)
- [animate.css](https://github.com/daneden/animate.css)


- Slick Animation
- https://codepen.io/neetee/pen/mddazOO?editors=1010
- https://github.com/marvinhuebner/slick-animation

## Documentation


## Html Markup

```html
<div class="slider-active">
    <div class="single-slider">
        <h2 data-animation="fadeInUp" data-delay="1.2s">
            Lorem ipsum dolor sit amet.
        </h2>
        <p data-animation="fadeInUp" data-delay="0.4s">
            Lorem ipsum dolor sit amet At vero eos et accusam et justo duo dolores et ea rebum. no sea takimata sanctus est Lorem ipsum dolor sit amet. sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
        </p>
    </div>
    <div class="single-slider">
        <h2 data-animation="fadeInUp" data-delay="0.2s">
            Lorem ipsum dolor sit amet.
        </h2>
        <p data-animation="fadeInUp" data-delay="0.4s">
            Lorem ipsum dolor sit amet At vero eos et accusam et justo duo dolores et ea rebum. no sea takimata sanctus est Lorem ipsum dolor sit amet. sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
        </p>
    </div>
    <div class="single-slider">
        <h2 data-animation="fadeInUp" data-delay="0.2s">
            Lorem ipsum dolor sit amet.
        </h2>
        <p data-animation="fadeInUp" data-delay="0.4s">
            Lorem ipsum dolor sit amet At vero eos et accusam et justo duo dolores et ea rebum. no sea takimata sanctus est Lorem ipsum dolor sit amet. sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
        </p>
    </div>
</div>
```

## Js Code

```js

if (jQuery(".slider-active").length > 0) {

    var BasicSlider = $('.slider-active');
	BasicSlider.on('init', function (e, slick) {
		var $firstAnimatingElements = $('.single-slider:first-child').find('[data-animation]');
		doAnimations($firstAnimatingElements);
	});
	BasicSlider.on('beforeChange', function (e, slick, currentSlide, nextSlide) {
		var $animatingElements = $('.single-slider[data-slick-index="' + nextSlide + '"]').find('[data-animation]');
		doAnimations($animatingElements);
	});
	BasicSlider.slick({
		autoplay: true,
		autoplaySpeed: 10000,
		dots: false,
		fade: true,
		arrows: true,
		prevArrow: '<button type="button" class="slick-prev"><i class="fal fa-angle-left"></i></button>',
		nextArrow: '<button type="button" class="slick-next"><i class="fal fa-angle-right"></i></button>',
		responsive: [
			{ breakpoint: 992, settings: { dots: false, arrows: false } }
		]
	});

	function doAnimations(elements) {
		var animationEndEvents = 'webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend';
		elements.each(function () {
			var $this = $(this);
			var $animationDelay = $this.data('delay');
			var $animationType = 'animated ' + $this.data('animation');
			$this.css({
				'animation-delay': $animationDelay,
				'-webkit-animation-delay': $animationDelay
			});
			$this.addClass($animationType).one(animationEndEvents, function () {
				$this.removeClass($animationType);
			});
		});
	}
}
```

## Js Code (Vertical Slider)

```js
if (jQuery(".slider-active").length > 0) {
    $('.slider-active').slick({
        appendArrows: false,
        dots: true,
        infinite: true,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 1,
        autoplay: true,
        autoplaySpeed: 5000,
        vertical: true,
        centerMode: true,
        centerPadding: '0',
        verticalSwiping: true,
    });
}
```

## Js Code (Carousel Slider)

```js
	$('.slider-active').slick({
	slidesToShow: 5,
	slidesToScroll: 1,
	dots: true,
	arrows: false,
	centerMode: true,
	centerPadding: 0,
	autoplay:true,
	responsive: [
		{
			breakpoint: 1200,
			settings: {
				slidesToShow: 3,
				slidesToScroll: 1
			}
		},
		{
			breakpoint: 992,
			settings: {
				slidesToShow: 3,
				slidesToScroll: 1
			}
		},
		{
			breakpoint: 768,
			settings: {
				slidesToShow: 2,
				slidesToScroll: 2
			}
		},
		{
			breakpoint: 560,
			settings: {
				slidesToShow: 1,
				slidesToScroll: 1
			}
		}
	]
});
```