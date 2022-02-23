# The Final Countdown

- http://hilios.github.io/jQuery.countdown/


## Documentation

- http://hilios.github.io/jQuery.countdown/documentation.html


## Html Markup

```html

<!-- event-timer start -->
<div class="event-timer mt-20">
    <div data-countdown="2021/04/01"></div>
</div>
<!-- event-timer end -->

```

## Js Code

```js

/*------------------------------------
    countdown
--------------------------------------*/
if (jQuery("[data-countdown]").length > 0) {
    $('[data-countdown]').each(function () {
        var $this = $(this), finalDate = $(this).data('countdown');
        $this.countdown(finalDate, function (event) {
            $this.html(event.strftime('<span class="cdown days"><p>Days</p> <span class="time-count">%-D</span></span> <span class="cdown hour"><p>Hour</p> <span class="time-count">%-H</span></span> <span class="cdown minutes"><p>Min</p> <span class="time-count">%M</span></span> <span class="cdown second"><p>Sec</p> <span><span class="time-count">%S</span></span>'));
        });
    });
}


```

## Scss Code

```scss

.cdown {
    display: inline-block;
    width: 110px;
    text-align: center;
    font-weight: 500;
    padding: 18px 0;
    background: #fff;
    margin-right: 25px;
    border-right: 4px solid $theme-color;
    border-bottom: 4px solid $theme-color;
    margin-bottom: 30px;

    &:last-child{
        margin-right: 0;
    }

    @include mq(lg){
        width: 100px;
    }

    span {
        font-size: 43px;
        color: $theme-color;
        line-height: 1;
        display: block;
        margin-bottom: 0;
        font-weight: 600;
        font-family: $Signika;
        @include mq(lg){
            font-size: 36px;
        }
    }

    p {
        font-size: 14px;
        color: #363636;
        line-height: 1;
        margin-bottom: 14px;
        text-transform: uppercase;
        font-weight: 600;
        letter-spacing: 1px;
    }
}


```