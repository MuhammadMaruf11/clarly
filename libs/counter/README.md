# Odometer Counter

- https://github.com/HubSpot/odometer

## Documentation

- [odometer](https://github.hubspot.com/odometer/docs/welcome/)

## Html Markup

```html
<div class="counter-wrap mb-30">
	<h3><span class="odometer" data-count="890">00</span>+</h3>
	<p>Happy Customers</p>
</div>
<!--    Slide Bar End    -->
```

## Js Code (Active Menu)

```js
/*------------------------------------
	Odometer Counter
--------------------------------------*/
$('.odometer').appear(function (e) {
	var odo = $(".odometer");
	odo.each(function () {
		var countNumber = $(this).attr("data-count");
		$(this).html(countNumber);
	});
});
```