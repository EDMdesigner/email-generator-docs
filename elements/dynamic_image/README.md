Dynamic image element

Dynamic images are the same as images in the output HTML, the difference is that you have to add the URL and the altText manually, and it must contain an expression.
You can set the width and the height to any value, but you have to make sure that you will use images with the same dimensions.
In the editor and in the preview a placeholder image is going to be shown.

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
	"altText" : "cactii",
	"customData" : {},
	"src" : "https://example.com/images/?image={{user_id}}",
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
altText | string | text | a short, descriptive text about the used image
customData | object | object| editor related property [Read more](customData/README.md)
src | string | the url of the image, it must contain a valid expression
link | string | url | with this property the image can be wrapped in a link
mini | | boolean | editor related property (it is not necessary)

