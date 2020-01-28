Th full width container is the base element of the document. It can only be a direct child of the root, so can be placed only in the highest level of the document structure. The main feature of this element type is that the adjusted background color and/or image extends to the full width of the email client's view pane. 

There is a new feature in the genertor, is it possible to add the full width container's inner fixed width container a different width (before that the full width container's width property was set to 600px wide). Now it's is possible to set every full width block individually wider than the usual 600px.

```
{
	"root" : {
		"children" : [ 
			{
				"type" : "FULLWIDTH_CONTAINER",
				"background" : {
					"image" : {
						"src" : "https://example.png",
						"repeat" : "no-repeat",
						"position" : "center center"
					},
					"color" : "#60de55"
				},
				"width" : 600,
				"children" : [ 
					...
				]

				"hideOnMobile" : false,
				"customData" : {},
				"hideOnDesktop" : false
		}
	],
	"type" : "ROOT"
}
```

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| background | object |  |[Read more](../../property-groups/background/README.md)
| width | number | integer | the width of the content block (if the whole content placed inside one full width container that is equal to the email's body) can be set here in pixels |
children | array |  | The children array may [contain any of our element types](/elements) except the full-width element. |
|hideOnMobile | string  | boolean | if it set to `true`, the container won't show on mobile view |
|hideOnDesktop | string  | boolean | if it set to `true`, the container won't show on desktop view |


Note:
There was a two-cell format functionality on the full width container in the EDMdesigner editor, but this became deprecated in order to handle VML background images. The new generator won't render this kind of layout.

However, here is a short explanation of this format:

"A fullwidth container can have 1 cell, or one left cell and one right cells divided from the middle. The cells can have their own background color. The elem can be set “left to right” or “right to left”. In case of “left to right” setting the left cells will be ordered on the top if there is no enough room for both in the same line. In case of “right to left” the right cell will do so. If the element is set to be 1 celled, the order property determines that which cell is displayed. The content of the not visible cell always will be stored so will never be lost only not displayed."

```
	"twoCell" : false,
	"isLeftHigher" : true,
	"order" : "LTR",
```