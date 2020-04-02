

```
{
	"type" : "SOCIAL",
	"elements" : [ 
		{
			"type" : "facebook",
			"link" : "",
			"src" : "img/Facebook/fb-4-colorful.png"
		}, 
	...
	],
	"align" : "center",
	"color" : "colorful",
	"iconSet" : 4,
	"size" : 40,
	"layout" : "horizontal",
	"spacing" : 25,
	"hideOnMobile" : false,
	"hideOnDesktop" : false,
	"reorderOnMobile" : true,
	"baseUrl" : "https://plugins.edmdesigner.com/mega-editor/3.1.15/"
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
elements| 
align | string | left, center, right | set the position of the social icons inside their parent container
color | string | "colorful", "black", "grey", "white" | editor related property, 
iconset | number |  | editor related property
layout | string | "horizontal", "vertical" | set the position of the icons 
padding | object | object | [Read more](/property-groups/padding/README.md)
height | number | integer | the scaled width of the image
width | number | integer | the scaled width of the image
sizeType | string | FIXED | this editor related property only takes the value `FIXED` and it defined for the old generator to use te width property as a width attribute (it is not neccessary anymore)
originalHeight | number | integer | editor related property, it stores the original height property of the used image
originalWidth | number | integer| editor related property, it stores the original height property of the used image
altText | string | text | a short, descriptive text about the used image
customData | object | object| editor related property [Read more](customData/README.md)
src | string | url | the url of the image
link | string | url | with this property the image can be wrapped in a link
mini | | boolean | editor related property (it is not neccessary)

