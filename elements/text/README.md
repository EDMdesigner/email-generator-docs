There was a time, when sending HTML emails built from images was a common practice, but using image-based emails lead to a lot of problems, like exclude subscribers with vision impairment, poor internet connection or whom set the image blocking. It is essential to use as many live text as possible.

Keep in mind that there are lot of limitation on custom font usage, choose your font set wisely. [More on thet matter:](https://chamaileon.io/resources/best-fonts-for-email/)

The generator has a bulit in fallback font stack for word based Outlooks, because without it the default font family was Times New Roman. 

```
{
	"type": "TEXT",
	"text": "<p><span style="font-size:18px;">example text</span></p><p>&nbsp;</p>",
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
typography | object | object | it contains the basic typography properties set in the editor
typography.h* | object | object | it contains the font properties of the different headers
typography.h*.family | string | font-family name | set the font-family style of the header
typography.h*.size | number | integer | set the font size of the header (good practice is using even numbers, because outlooks have a bug and sometimes show thin lines under elements that has have odd font size or padding value)
typography.h*.color | string | hex code | set the color of the chosen font of the header
typography.h*.lineHeight | number | integer | set the lineheight of the chosen font of the header
typography.h*.weight | string | normal, bold | set the weight of the chosen font of the header
typography.h*.style | string | normal, italic | set the style of the chosen font of the header
typography.text | object | object | it contains the font properties of the value of the text property
ypography.text.family | string | font-family name | set the font-family style of the value of the text property
typography.text.size | number | integer | set the font size of the value of the text property (good practice is using even numbers, because outlooks have a bug and sometimes show thin lines under elements that has have odd font size or padding value)
typography.text.color | string | hex code | set the color of the chosen font of the value of the text property
typography.text.lineHeight | number | integer | set the lineheight of the chosen font of the value of the text property
typography.text.weight | string | normal, bold | set the weight of the chosen font of the value of the text property
typography.text.style | string | normal, italic | set the style of the chosen font of the value of the text property
typography.link | object | object | specifies the links styles for those `<a>` tags what has no inline style
typography.link.color | string | hex code | set the color of the linked text
typography.link.underline |  | boolean | if it set to `true`, the linked text will be underlined to indicate that part of the text is a hyperlink 
typography.spacing | object | object | set the spacing around the text content 
typography.spacing.top | number | integer | set the spacing on the top of the text content

*= h1-h6