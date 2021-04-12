# Button element

Buttons are usually used for call-to-actions and are one of the most important elements of the email. It's used to refer to an instruction or a request that a company makes to its audience in order to provoke a certain response or action.

Buttons are relatively complex as well. It can have the following box properties: paddings, margins, borders, backgrounds (color and background image as well). In addition it can have radius. The most important property of a button is the link value of the href property and the text.

```
{
	"type":"BUTTON",
	"padding":{
		...
	},
	"margin":{
		...
	},
	"border":{
		...
	},
	"background":{
		...
	},
	"align": "right",
	"width": 112,
	"fullWidthOnMobile": true,
	"text":"<span style="font-family:Tahoma; font-size:16px">Button</span>",
	"href":"https://example.com",
	"sizeType":"FIXED",
	"typography":{
		"text":{
			"family":"arial",
			"size":16,
			"color":"#000000",
			"lineHeight":20,
			"weight":"normal",
			"style":"normal"
		}
	}
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
align | string | left, center, right | set the position of the button inside its parent container
background | oject | object | [Read more](/property-groups/border/README.md)
margin | object | object | [Read more](/property-groups/margin/README.md)
border | object | object | [Read more](/property-groups/border/README.md)
padding | object | object | [Read more](/property-groups/padding/README.md)
width | number | integer | the width of the button, if the sizeType property doesn't have the value "FIXED"
fullWidthOnMobile | | boolean | if it's set to `true`, the width of the button extends to the full width of the mobile's view pane
sizeType | string | FIXED, FIT_TO_TEXT | if it's set to “FIXED”: the width of the button will be the previously declared width value in pixels, if it set to “FIT_TO_TEXT”: the width will be based on the width of the text
text | string | text | the text that should appear on the button *(it can be a simple valid html snippet as well, the generator can handle that as well)*
href | string | link | 
typography | object | object | it contains the basic typography properties set in the editor
typography.text | object | object | 
typography.text.family | string | font-family name | set the font-family style of the button
typography.text.size | number | integer | set the font size of the button *(good practice is to use even numbers, because Outlook clients have a bug and sometimes they show thin lines under elements that have odd font sizes or padding values)*
typography.text.color | string | hex code | set the color of button's font
typography.text.lineHeight | number | integer | set the line-height of button's font
typography.text.weight | string | normal, bold | set the weight of button's font
typography.text.style | string | normal, italic | set the style of button's font