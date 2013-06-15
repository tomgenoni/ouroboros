# Ouroboros Sass/CSS Spinner

See blog entry at [http://atomeye.com/projects/sass-css-spinner.html](http://atomeye.com/projects/sass-css-spinner.html) for more details.

The Ouroboros is an ancient symbol depicting a serpent or dragon eating its own tail. Inspired by application progress spinners this provides an imageless 'throbber' for modern browsers that eats itself (in a way).
The name comes after the greek words ουρά (tail) + βόρος (eater / devourer).

## Browser Support

- Chrome 24+
- Firefox 18+
- IE 10+
- Opera 12+
- Safari 5+
- iOS 5 &amp; 6 (scrolling pauses animation)

A standard 32x32 animated gif throbber is provided as a fallback for older versions of IE. It is centered where the spinner animation would have been.

## Usage

1. For Sass users add the `_ui-spinner.scss` into your project.
2. If you want IE < 10 support also add the `spinner-old-ie.scss` and the throbber.gif. You can include it with an IE conditional tag. See the example in `index.html`.

```html
<!--[if IE]>
	<link media="screen" type="text/css" href="stylesheets/spinner-old-ie.css" rel="stylesheet" />
<![endif]-->
```

3. In our project Sass use the `ui-spinner` mixin with defaults or pass in any arguments. Also see the mixin examples in `example.scss`.

```scss
@include ui-spinner; // Will use defaults.
@include ui-spinner(#fff, 60px, gray, purple, .7, 4s); // Will use these variables.
```

4. Use with the following HTML. Also see the HTML examples in `index.html`.

```html
<div class="ui-spinner">
	<span class="side side-left">
		<span class="fill"></span>
	</span>

	<span class="side side-right">
		<span class="fill"></span>
	</span>
</div>
```

### The 6 Optional Parameters

<table>
	<tr>
		<th>Parameter</th>

		<th>Description</th>

		<th>Defaults</th>
	</tr>

	<tr>
		<td>Hole color*</td>

		<td>Color of the hole to fake a ring</td>

		<td>transparent</td>
	</tr>

	<tr>
		<td>Size</td>

		<td>Size of the spinner</td>

		<td>46px</td>
	</tr>

	<tr>
		<td>Background color light</td>

		<td>First color, specify a lighter of the two colors</td>

		<td>#ddd</td>
	</tr>

	<tr>
		<td>Background color dark</td>

		<td>Second color, specify the darker of the two colors</td>

		<td>#3c76ca</td>
	</tr>

	<tr>
		<td>Opacity</td>

		<td>The opacity of the spinner</td>

		<td>.8</td>
	</tr>

	<tr>
		<td>Duration</td>

		<td>Speed of the spinner</td>

		<td>3s</td>
	</tr>
</table>

* The hole color is just to fake a ring spinner. You have to match the color you pass into the mixin to the background-color that the spinner will appear against.

## Don't Use Sass?

You can use the CSS that the Sass generates in `stylesheets/main.scss` and make edits to the parameters described above.
