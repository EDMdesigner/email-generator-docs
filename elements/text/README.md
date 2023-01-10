# Text element

There was a time, when sending HTML emails built from images was a common practice, but using image-based emails lead to a lot of problems, like excluding subscribers with vision impairment, poor internet connection or if they set the images to be blocked. It is essential to use as many live text elements as possible.

Keep in mind that there are a lot of limitations on custom font usage, choose your font set wisely. [More on that matter:](https://chamaileon.io/resources/best-fonts-for-email/)

The generator has a built in fallback font stack for word based Outlooks, because without it the default font family is Times New Roman.

There is a new feature in the generator, it is possible to add a background image directly to the `text` element. The generator places the text inside a wrapper table and the background settings are applied on that table.

```json
{
	"type": "TEXT",
	"text": "<p><span style=\"font-size:18px;\">example text</span></p><p>&nbsp;</p>",
	"background":{
		"image":{
			"src":"http://example.jpg",
			"repeat":"no-repeat",
			"position":"center center"
		},
		"color":"#60de55"
	},
	"typography": {
		"h1": {
			"family": "arial",
			"size": 32,
			"color" :"#000000",
			"lineHeight": 32,
			"weight": "bold",
			"style": "normal"
		},
		"h2": {
			"family": "arial",
			"size": 26,
			"color": "#000000",
			"lineHeight": 26,
			"weight": "bold",
			"style": "normal"
		},
		"h3": {
			"family": "arial",
			"size": 22,
			"color": "#000000",
			"lineHeight": 22,
			"weight": "bold",
			"style": "normal"
		},
		"h4": {
			"family": "arial",
			"size": 20,
			"color": "#000000",
			"lineHeight": 20,
			"weight": "bold",
			"style": "normal"
		},
		"h5": {
			"family": "arial",
			"size": 18,
			"color": "#000000",
			"lineHeight": 18,
			"weight": "bold",
			"style": "normal"
		},
		"h6": {
			"family": "arial",
			"size": 16,
			"color":" #000000",
			"lineHeight": 16,
			"weight": "bold",
			"style": "normal"
		},
		"text": {
			"family": "arial",
			"size": 14,
			"color": "#000000",
			"lineHeight": 14,
			"weight": "normal",
			"style": "normal"
		},
		"link":{
			"color": "#5555ff",
			"underline": true
		}
	},
	"spacing":{
		"top":5,
		"right":5,
		"bottom":5,
		"left":5
	}
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
text | string | text | the content text that can be a valid short HTML code snippet |
background | object | object | [Read more](/property-groups/background/README.md)
typography | object | object | it contains the basic typography properties set in the editor
typography.h* | object | object | it contains the font properties of the different headers
typography.h*.family | string | font-family name | set the font-family style of the header
typography.h*.size | number | integer | set the font size of the header *(good practice is to use even numbers, because Outlook clients have a bug and sometimes they show thin lines under elements that have odd font sizes or padding values)*
typography.h*.color | string | hex code | set the color of the chosen header font
typography.h*.lineHeight | number | integer | set the line-height of the chosen header font
typography.h*.weight | string | normal, bold | set the weight of the chosen header font
typography.h*.style | string | normal, italic | set the style of the chosen header font
typography.text | object | object | this contains the font properties for the text element font
typography.text.family | string | font-family name | set the font-family style for the text element font
typography.text.size | number | integer | set the font size for the text element font *(good practice is to use even numbers, because Outlook clients have a bug and sometimes they show thin lines under elements that have odd font sizes or padding values)*
typography.text.color | string | hex code | set the color for the text element font
typography.text.lineHeight | number | integer | set the line-height for the text element font
typography.text.weight | string | normal, bold | set the weight for the text element font
typography.text.style | string | normal, italic | set the style for the text element font
typography.link | object | object | specifies the links styles for those `<a>` tags that have no inline styling
typography.link.color | string | hex code | set the color of the linked text
typography.link.underline |  | boolean | if it's set to `true`, the linked text will be underlined to indicate that part of the text is a hyperlink
typography.spacing | object | object | set the spacing around the text content
typography.spacing.top | number | integer | set the spacing on the top of the text content

*= h1-h6
