# Metis Menu

- https://github.com/onokumus/metismenu

## Documentation

- [metismenu](https://mm.onokumus.com/)

## Html Markup

```html
<!--    Slide Bar Start   -->
<aside class="slide-bar">
	<div class="close-mobile-menu">
		<a href="javascript:void(0);"><i class="fas fa-times"></i></a>
	</div>
	<nav class="side-mobile-menu">
		<ul id="mobile-menu-active">
			<li><a href="#">home</a></li>
			<li><a href="#">service</a></li>
			<li><a href="#">about</a></li>
			<li class="has-children"><a href="#">elements</a>
				<ul>
					<li><a href="#">Typography</a></li>
					<li><a href="#">Buttons</a></li>
					<li><a href="#">Progress Bars</a></li>
				</ul>
			</li>
			<li class="has-children"><a href="#">Menu lev 1</a>
				<ul>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li><a href="#">Menu lev 2</a></li>
					<li class="has-children"><a href="#">Menu lev 2</a>
						<ul>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
							<li><a href="#">Menu lev 3</a></li>
						</ul>
					</li>
					<li><a href="#">Menu lev 2</a></li>
				</ul>
			</li>
			<li><a href="#">Contact</a></li>
		</ul>
	</nav>
</aside>
<div class="body-overlay"></div>
<!--    Slide Bar End    -->
```

## Js Code (Active Menu)

```js
	/*------------------------------------
		Mobile Menu
	--------------------------------------*/
	$('#mobile-menu-active').metisMenu();

	$(".open-mobile-menu > a").on("click", function (e) {
		e.preventDefault();
		$(".slide-bar").toggleClass("show");
		$("body").addClass("on-side");
		$('.body-overlay').addClass('active');
		$(this).addClass('active');
	});

	$(".close-mobile-menu > a").on("click", function (e) {
		e.preventDefault();
		$(".slide-bar").removeClass("show");
		$("body").removeClass("on-side");
		$('.body-overlay').removeClass('active');
		$('.open-mobile-menu > a').removeClass('active');
	});

	$('.body-overlay').on('click', function () {
		$(this).removeClass('active');
		$(".slide-bar").removeClass("show");
		$("body").removeClass("on-side");
		$('.open-mobile-menu > a').removeClass('active');
	});
```