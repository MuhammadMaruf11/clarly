# Owl Carousel

- https://owlcarousel2.github.io/OwlCarousel2/

## Dependencies

- [owl.carousel](https://github.com/OwlCarousel2/OwlCarousel2/)
- [animate.css](https://github.com/daneden/animate.css)

## Documentation

- https://owlcarousel2.github.io/OwlCarousel2/docs/started-installation.html
- https://owlcarousel2.github.io/OwlCarousel2/docs/api-options.html

## Html Markup

```html
<div class="slider-active owl-carousel">
    <div class="item">
        <h2 data-animation="fadeInUp" data-delay="0.2s">
            Lorem ipsum dolor sit amet.
        </h2>
        <p data-animation="fadeInUp" data-delay="0.4s">
            Lorem ipsum dolor sit amet At vero eos et accusam et justo duo dolores et ea rebum. no sea takimata sanctus est Lorem ipsum dolor sit amet. sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
        </p>
    </div>
    <div class="item">
        <h2 data-animation="fadeInUp" data-delay="0.2s">
            Lorem ipsum dolor sit amet.
        </h2>
        <p data-animation="fadeInUp" data-delay="0.4s">
            Lorem ipsum dolor sit amet At vero eos et accusam et justo duo dolores et ea rebum. no sea takimata sanctus est Lorem ipsum dolor sit amet. sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat.
        </p>
    </div>
    <div class="item">
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

    let carousel_slider = $(".slider-active");
    carousel_slider.owlCarousel({
        items: 1,
        loop: true,
        nav: true,
        navText: ['<i class="fas fa-chevron-left"></i>','<i class="fas fa-chevron-right"></i>'],
        dots: true,
        animateOut: 'fadeOut',
        animateIn: 'fadeIn',
        autoplay: true,
        autoplayTimeout: 10000,
    });

    carousel_slider.on('translate.owl.carousel', function () {
        let slideLayer = $("[data-animation]");
        slideLayer.each(function () {
            let anim_name = $(this).data('animation');
            $(this).removeClass('animated ' + anim_name).css('opacity', '0');
        });
    });

    carousel_slider.on('translated.owl.carousel', function () {
        let slideLayer = carousel_slider.find('.owl-item.active').find("[data-animation]");
        slideLayer.each(function () {
            let anim_name = $(this).data('animation');
            $(this).addClass('animated ' + anim_name).css('opacity', '1');
        });
    });

    $("[data-delay]").each(function () {
        let anim_del = $(this).data('delay');
        $(this).css('animation-delay', anim_del);
    });

    $("[data-duration]").each(function () {
        let anim_dur = $(this).data('duration');
        $(this).css('animation-duration', anim_dur);
    });
}
```