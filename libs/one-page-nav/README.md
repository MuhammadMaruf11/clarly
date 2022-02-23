# One Page Nav

- https://davist11.github.io/jQuery-One-Page-Nav/


## Documentation

- https://github.com/davist11/jQuery-One-Page-Nav


## Html Markup

```html

<div class="primary-menu">
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">page</a></li>
        <li><a href="#">Service</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">contact</a></li>
    </ul>
</div>

```

## Js Code

```js

// One Page Nav
var top_offset = $('.header-area').height() - 10;
$('.main-menu nav ul').onePageNav({
	currentClass: 'active',
	scrollOffset: top_offset,
});


```
