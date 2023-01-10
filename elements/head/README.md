# Head property

The `head` property is part of the new properties that helps to keep the JSON file more organized. The `head` contains properties that will be placed in the `<head>` tag of the generated email HTML file.
In the old JSON format of our editors these properties were placed in various parts of the files, but there is no need to change that, because the new generator will convert it. These are the still supported methods to add custom fonts:
 - There is an option in the EDMdesigner API dashboard where you can add the google font resource and that link will be placed in a `<link>` meta tag in the `head`.  There is a placeholder in the raw HTML file's head tag for that purpose:
`<!--##custom-font-resource##-->`
 - There is a stack of supported google fonts built into the Chamaileon editor, if you use any of them, there is no need to place the link anywhere in the JSON file.

A main change compared to the older versions is how to define the used fonts, if they are used from an external source and are not one of the web safe fonts. It needs to be inserted into an array called `fonts` and it should be an object that defines the name and source for the used font.
Be aware that not every email client supports web fonts and custom fonts, always define a fallback font in the typography property of the elements.
[Read more on supported fonts](https://chamaileon.io/resources/best-fonts-for-email/#quick_guide_to_web_fonts_and_web-safe_fonts)
[Read more on typography](../text/README.md)

Example for the new format:
```json
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
head | object | object | this property contains the properties that will be placed inside the `head` tag of the HTML
head.fonts| array |  | an array containing objects that define the font with the name and a source for it.
head.fonts[].name | string | font family name | the font-family name can be set here
head.fonts[].href | string | link | you can set the path for the font-family here
head.title | string | text | set a title that is shown in the "show online" versions [Read more](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title)
