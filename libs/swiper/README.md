# Swiper Slider

- https://swiperjs.com/


## Documentation
- https://swiperjs.com/demos/
- https://swiperjs.com/api/


## Html Markup

```html
<div class="slider-active-wrap">
	<div class="swiper-container">
		<!-- Additional required wrapper -->
		<div class="swiper-wrapper">
			<div class="swiper-slide single-slide">
				<div class="container">
					<div class="row">
						<div class="col-xl-10 col-lg-8 col-xl-6">
							<div class="slider-content-1">
								<span data-animation="fadeInUp" data-delay="0.3s">
									Making Different Form Others
								</span>
								<h2 data-animation="fadeInUp" data-delay="0.6s">Build A Perferct Health
									Growth</h2>
								<a href="#" class="btn btn-gra" data-animation="fadeInUp" data-delay="0.9s">
									join with us
									<i class="fas fa-angle-double-right"></i>
								</a>
							</div>
						</div>
					</div>
				</div>
			</div>
			<div class="swiper-slide single-slide">
				<div class="container">
					<div class="row">
						<div class="col-xl-10 col-lg-8 col-xl-6">
							<div class="slider-content-1">
								<span data-animation="fadeInUp" data-delay="0.3s"> Different Form Others </span>
								<h2 data-animation="fadeInUp" data-delay="0.6s">Build A Perferct Health
									Growth</h2>
								<a href="#" class="btn btn-gra" data-animation="fadeInUp" data-delay="0.9s">
									join with us
									<i class="fas fa-angle-double-right"></i>
								</a>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
	<!-- If we need pagination -->
	<div class="swiper-pagination"></div>
	<!-- If we need navigation buttons -->
	<div class="swiper-button-prev"><i class="far fa-angle-left"></i></div>
	<div class="swiper-button-next"><i class="far fa-angle-right"></i></div>
</div>
```


## Scss Markup

```scss
.slider-active-wrap {
	
	.swiper-pagination-fraction {
		position: absolute;
		left: 370px;
		width: auto;
		bottom: 60px;
		z-index: 99;
		font-family: "Teko", sans-serif;
		font-weight: 600;
		font-size: 20px;
		color: #333333;
		@include mq(xl) {
			left: 100px;
		}
		@include mq(lg) {
			left: 100px;
		}
		@include mq(md) {
			left: 80px;
		}
		@include mq(xs) {
			display: none;
		}

		.swiper-pagination-total {
			color: #b5b5b5;
		}
	}

	.swiper-pagination-clickable {
		position: absolute;
		left: 370px;
		width: auto;
		bottom: 80px;
		z-index: 99;
		transform: inherit;
		@include mq(xl) {
			left: 100px;
		}
		@include mq(lg) {
			left: 100px;
		}
		@include mq(md) {
			left: 80px;
		}
		@include mq(xs) {
			display: none;
		}

		.swiper-pagination-bullet {
			background: transparent;
			width: 25px;
			height: 25px;
			opacity: 1;
			border: 2px solid transparent;
			position: relative;
			z-index: 1;
			display: inline-block;
			@include transition(0.3s);

			&:before {
				content: "";
				width: 10px;
				height: 10px;
				position: absolute;
				left: 50%;
				top: 50%;
				z-index: -1;
				background: #fff;
				border-radius: 50%;
				transform: translate(-50%, -50%);
			}
		}

		.swiper-pagination-bullet-active {
			border-color: #fff;
		}
	}

	.swiper-button-prev {
		left: 50%;
		height: 70px;
		width: 70px;
		font-size: 20px;
		color: #666565;
		background: #fff;
		z-index: 99;
		margin: 0 0 0 -35px;
		bottom: 0;
		top: auto;
		transform: translateX(-50%);
		@include transition(0.3s);
		@include mq(md) {
			display: none;
		}
		@include mq(xs) {
			display: none;
		}

		&:hover {
			color: #fff;

			&:before {
				visibility: visible;
				opacity: 1;
			}
		}

		&:before {
			content: "";
			width: 100%;
			height: 100%;
			position: absolute;
			top: 0;
			left: 0;
			z-index: -1;
			visibility: hidden;
			opacity: 0;
			background: #e73e36;
			background-image: -moz-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			background-image: -webkit-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			background-image: -ms-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			@include transition(0.3s);
		}
	}

	.swiper-button-next {
		right: 50%;
		height: 70px;
		width: 70px;
		font-size: 20px;
		color: #666565;
		background: #fff;
		z-index: 99;
		margin: 0 -35px 0 0;
		bottom: 0;
		top: auto;
		transform: translateX(50%);
		@include transition(0.3s);
		@include mq(md) {
			display: none;
		}
		@include mq(xs) {
			display: none;
		}

		&:hover {
			color: #fff;

			&:before {
				visibility: visible;
				opacity: 1;
			}
		}

		&:before {
			content: "";
			width: 100%;
			height: 100%;
			position: absolute;
			top: 0;
			left: 0;
			z-index: -1;
			visibility: hidden;
			opacity: 0;
			background: #e73e36;
			background-image: -moz-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			background-image: -webkit-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			background-image: -ms-linear-gradient(-72deg, rgb(230, 58, 52) 0%, rgb(238, 115, 73) 99%);
			@include transition(0.3s);
		}
	}
}
```


## Js Code

```js
	/*------------------------------------
        Slider
	--------------------------------------*/
	if (jQuery(".slider-active-wrap").length > 0) {
		let sliderActive1 = '.slider-active-wrap';
		let sliderInit1 = new Swiper(sliderActive1, {
			// Optional parameters
			slidesPerView: 1,
			slidesPerColumn: 1,
			paginationClickable: true,
			loop: true,
			effect: 'fade',

			autoplay: {
				delay: 5000,
			},

			// If we need pagination
			pagination: {
				el: '.swiper-pagination',
				type: 'fraction',
				// clickable: true,
			},

			// Navigation arrows
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev',
			},

			a11y: false
		});

		function animated_swiper(selector, init) {
			let animated = function animated() {
				$(selector + ' [data-animation]').each(function () {
					let anim = $(this).data('animation');
					let delay = $(this).data('delay');
					let duration = $(this).data('duration');

					$(this).removeClass('anim' + anim)
						.addClass(anim + ' animated')
						.css({
							webkitAnimationDelay: delay,
							animationDelay: delay,
							webkitAnimationDuration: duration,
							animationDuration: duration
						})
						.one('webkitAnimationEnd mozAnimationEnd MSAnimationEnd oanimationend animationend', function () {
							$(this).removeClass(anim + ' animated');
						});
				});
			};
			animated();
			// Make animated when slide change
			init.on('slideChange', function () {
				$(sliderActive1 + ' [data-animation]').removeClass('animated');
			});
			init.on('slideChange', animated);
		}

		animated_swiper(sliderActive1, sliderInit1);
	}
```

## Slider With Thumbs

```js
	// Slider With Thumbs
	if (jQuery(".testimonial-slider-2 .swiper-container").length > 0) {
		let testimonialThumbs2 = new Swiper('.testimonial-thumbs-2', {
			loop: true,
			loopedSlides: 5, //looped slides should be the same
			spaceBetween: 30,
			slidesPerView: 4,
			freeMode: true,
			watchSlidesVisibility: true,
			watchSlidesProgress: true,
			breakpoints: {
				320: {
					slidesPerView: 2,
				},
				768: {
					slidesPerView: 4,
				},
				1024: {
					slidesPerView: 4,
				},
				1200: {
					slidesPerView: 4,
				},
			},
		});

		let testimonialSlider2 = new Swiper('.testimonial-slider-2 .swiper-container', {
			// Optional parameters
			slidesPerView: 1,
			slidesPerColumn: 1,
			paginationClickable: true,
			loop: true,
			loopedSlides: 5, //looped slides should be the same
			spaceBetween: 30,

			autoplay: {
				delay: 3000,
			},

			// Navigation arrows
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev',
			},

			thumbs: {
				swiper: testimonialThumbs2
			},

			a11y: false
		})

	}
```

## Slider With Scrollbar

```js
	// Slider With Scrollbar
	if (jQuery(".gallery-carousel .swiper-container").length > 0) {
		let gallerySlider1 = new Swiper('.gallery-carousel .swiper-container', {
			// Optional parameters
			slidesPerView: 1,
			slidesPerColumn: 1,
			paginationClickable: true,
			loop: true,
			spaceBetween: 30,

			autoplay: {
				delay: 3000,
			},

			scrollbar: {
				el: '.swiper-scrollbar',
				hide: true,
			},

			// Navigation arrows
			navigation: {
				nextEl: '.swiper-button-next',
				prevEl: '.swiper-button-prev',
			},

			a11y: false
		})
	}
```