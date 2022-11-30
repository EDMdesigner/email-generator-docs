# Fullwidth container element

The fullwidth container is the base element of the document. It can only be a direct child of the root, so it can only be placed at the highest level of the document structure. The main feature of this element type is that the adjusted background color and/or image extends to the full width of the email client's view pane.

There is a new feature in the generator, and it's possible to set the full width container's inner fixed width container to a different width (before that the full width container's width property was set to 600px wide). Now it is possible to set every full width block individually (for example: wider than the usual 600px).

```json
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
| width | number | integer | the width of the content block *(the whole content can be placed inside one fullwidth container that is equal to the email's body)* can be set here in pixels |
children | array |  | The children array may [contain any of our element types](/elements) except the fullwidth element. |
|hideOnMobile | string  | boolean | if it's set to `true`, the container won't show on mobile view |
|hideOnDesktop | string  | boolean | if it's set to `true`, the container won't show on desktop view |


Note:
There was a two-cell format functionality on the fullwidth container in the EDMdesigner editor, but this became deprecated in order to handle VML background images. The new generator won't render this kind of layout.

However, here is a short explanation of this format:

"A fullwidth container can have 1 cell, or one left cell and one right cell that are divided in the middle. The cells can have their own background color. The elem can be set “left to right” or “right to left”. In case of “left to right” setting the left cells will be ordered on the top if there is not enough room for both in the same line. In case of “right to left” the right cell will do the same. If the element is set to have 1 cell, the order property determines that which cell is displayed. The content of the invisible visible cell is going be stored so it will never be lost, only it's not displayed."

```
	"twoCell" : false,
	"isLeftHigher" : true,
	"order" : "LTR",
```
