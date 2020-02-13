The `head` property is part of the new properties that help keeping the JSON file more organised. The `head` contains properties that will be placed in the `<head>` tag of the generated email HTML file.
In the old JSON format of our editors these properties were placed in various parts of the files, but there is no need to change that, because the new generator will convert it.

A main change compared to the older versions is how to define the used fonts, if they are used from an external source and not one of the web safe fonts. It need to be placed in an array called fonts and put the name and source of the used fonts organised in objects.
Be aware not every email client support webfonts and custom fonts, always define a fallback font in the typography propery of the elements.
[Read more on supported fonts](https://chamaileon.io/resources/best-fonts-for-email/#quick_guide_to_web_fonts_and_web-safe_fonts)
[Read more on typography](../text/README.md)

Example for the new format:
```
{
	"head": {
		"fonts": [
			{
				"name": "Arvo",
				"href": "https://fonts.googleapis.com/css?family=Arvo"
			},
			{
				"name": "Avenir",
				"href": "https://fonts.googleapis.com/css?family=Avenir"
			}
		],
		"title": "example text"
	}
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
head | object | object | this property contains the properies that will be placed inside the `head` tag of the HTML
head.fonts| array |  | set objects inside with the name and a source of the used fonts
head.fonts.name | string | font family name | set here the name of the  font family that used in the email
head.fonts.href | string | link | set here the path of the  font family that used in the email
head.title | string | text | set a title that is shown in the "show online" versions [Read more](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)