# Image element

Images are one of the most important design elements of a commercial email, but they should be used with caution. [More on that](https://blog.edmdesigner.com/12-extremely-easy-tips-for-effective-use-of-images-in-email-design/)

Images are relatively complex elements. Just like boxes, they can have paddings, margins, borders, background color (no background image property, because it would not have a good fallback resolution to set the same image as background, because of the poor client support of the background image), and they can’t have children.

```
{
	"type" : "IMAGE",
	"align" : "center",
	"background" : {
		"color" :"#60de55"
	},
	"border" : {
		...
		},
	},
	"margin" : {
		...
	},
	"padding" : {
		...
	},
	"height" : 300,
	"width" : 310,
	"sizeType" : "FIXED",
	"originalHeight" : 300,
	"originalWidth" : 300,
	"altText" : "cactii",
	"customData" : {},
	"src" : "https://example.com",
	"link" : "https://example.com",
	"mini" : false
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
align | string | left, center, right | set the position of the image inside its parent container
background.color | string | hex code | set a fallback color, if the image is disabled or not reachable
margin | object | object | [Read more](/property-groups/margin/README.md)
border | object | object | [Read more](/property-groups/border/README.md)
padding | object | object | [Read more](/property-groups/padding/README.md)
height | number | integer | the scaled height of the image
width | number | integer | the scaled width of the image
sizeType | string | FIXED | this editor related property only takes the value `FIXED` and it's defined for the old generator to use the width property as a width attribute (it is not necessary anymore)
originalHeight | number | integer | editor related property, it stores the original height property of the used image
originalWidth | number | integer| editor related property, it stores the original width property of the used image
altText | string | text | a short, descriptive text about the used image
customData | object | object| editor related property [Read more](customData/README.md)
src | string | url | the url of the image
link | string | url | with this property the image can be wrapped in a link
mini | | boolean | editor related property (it is not necessary)

