# The Final Countdown

- https://github.com/aterrien/jQuery-Knob


## Documentation

- http://anthonyterrien.com/demo/knob/


## Html Markup

```html

<!-- circle-progress start -->
<div class="progress-circular">
    <input type="text" class="knob" value="0" data-rel="75" data-linecap="round"
           data-width="200" data-bgcolor="#ffffff" data-fgcolor="#7dc642" data-thickness=".12" data-readonly="true" disabled/>
    <h4>Gardern Care</h4>
    <p>
        But must explain to you how
        all this mistaken idedenouncing pleasure and praising pain
    </p>
</div>
<!-- circle-progress end -->

```

## Js Code

```js

/*------------------------------------
    Circle Bars - Knob
--------------------------------------*/
if (typeof ($.fn.knob) != 'undefined') {
    $('.knob').each(function () {
        let $this = $(this),
            knobVal = $this.attr('data-rel');
        
        $this.knob({
            'draw': function () {
                $(this.i).val(this.cv + '%')
            }
        });
        
        $this.appear(function () {
            $({
                value: 0
            }).animate({
                value: knobVal
            }, {
                duration: 2000,
                easing: 'swing',
                step: function () {
                    $this.val(Math.ceil(this.value)).trigger('change');
                }
            });
        }, {
            accX: 0,
            accY: -150
        });
    });
}


```

## Scss Code

```scss

/* circle progress */

.progress-circular {
    margin-bottom: 30px;
    text-align: center;

    h4 {
        font-size: 26px;
        line-height: 28px;
        margin-bottom: 10px;
        margin-top: 30px;
        color: #363636;
    }

    p {
        font-size: 16px;
        line-height: 28px;
        color: #686868;
        margin-bottom: 0;
    }
}

.progress-circular.text-white {
    h4 {
        color: #fff;
    }

    p {
        color: #a0adc0;
    }
}


```