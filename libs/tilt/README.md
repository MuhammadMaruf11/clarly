# Tilt Js

- https://gijsroge.github.io/tilt.js/
- https://github.com/gijsroge/tilt.js

## Documentation


## Html Markup

```html
	<span data-tilt data-tilt-perspective="3000" data-tilt-max="50"></span>
	<span data-tilt data-tilt-perspective="3000" data-tilt-reset="false"></span>
	<span data-tilt data-tilt-perspective="3000" data-tilt-speed="1000"></span>
	<span data-tilt data-tilt-perspective="3000" data-tilt-scale="1.2"></span>
	<span data-tilt data-tilt-perspective="3000" data-tilt-axis="x"></span>
	<span data-tilt data-tilt-perspective="3000" data-tilt-axis="y"></span>

	<!-- data-tilt-<option name>="value" --> 
```

## Js Code

```js

if (jQuery(".js-tilt").length > 0) {
	$('.js-tilt').tilt({
		glare: true,
		maxGlare: .5
	});
}

```