# Color Switcher

https://github.com/obiPlabon/color-switcher

## Html Markup

```html
	
	<h1>Color Switcher Demo</h1>

	<link rel="stylesheet" href="dist/color-switcher.css">
	<script src="dist/color-switcher.js"></script>
	
    <script>
        var colorSheets = [
            {
                color: "#ff8400",
                title: "Switch to Default",
                href: "./css/color-default.css"
            },
            {
                color: "#ff463a",
                title: "Switch to Red",
                href: "./css/color-red.css"
            },
            {
                color: "#4bda28",
                title: "Switch to Green",
                href: "./css/color-green.css"
            },
            {
                color: "#4650dc",
                title: "Switch to Blue",
                href: "./css/color-blue.css"
            },
            {
                color: "#f41c54",
                title: "Switch to Magenta",
                href: "./css/color-magenta.css"
            }
        ];

        ColorSwitcher.init(colorSheets);
	</script>
	
```
