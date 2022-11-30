# Multi-column element

Multi-columns are the main elements for creating complex layouts. They can have multiple columns and every column has a children array that contains the properties of the content. The children array of the columns can contain every element except the fullwidth container. [Read more](//fullwidth_container/README.md)

The arrays in the “cols” array represent the columns. The minimum number of columns are 2 and it can be changed to as many as you need. We support max. 5 in our EDMdesigner editor, but there is no limitation built into the generator.

The columns can't have padding, margin and border properties, these properties need to be added to the elements inside the children array. [Read more on set these properies](../../property-groups)

There are new features in the generator, now it is possible to:
 - set background properties to the multi-column and/or the columns. (Keep in mind if generating `VML background` is set to `true` and you set the background image on both elements, on Outlook email clients only the multi-column's image is going to appear. [Read more on VML background](../../generator-settings/VMLbackground.md)
  - define a child element called `COL_SPACER` and with its `width` and `height` property you can set a spacing around the columns inside the multi-columns. (It creates a more predictable and unified layout across various email clients)

The width of the multi-column is set to 100% and extends to the full width of its parent element. The width of the child elements of the columns is calculated from the width of the multi-columns parent elements width.

Keep in mind that:
 - the sum of the child elements width (if the column contains an element with padding, margin and/or border width set on, these are count in too) can't exceed the parent elements width, because the last column might break into a new line. It applies to the column spacings too, the sum of the columns and column spacings width can't pass the 100%.
 - too long words in a paragraph might push out the width of the column and it can break the layout.

Example for a valid older JSON version:

```json
{
	"type" : "MULTICOLUMN",
	"hideOnMobile" : false,
	"hideOnDesktop" : false,
	"reorderOnMobile": true,
	"cols" : [
		{
			"children" : [
				...
			],
			"hideOnMobile" : false,
			"lock" : false,
			"width" : 33.3333333333333
		},
		{
			"children" : [
				...
			],
			"hideOnMobile" : false,
			"lock" : false,
			"width" : 33.3333333333333
		},
		{
			"children" : [
				...
			],
			"hideOnMobile" : false,
			"lock" : false,
			"width" : 33.3333333333333
		}
	]
}
```

Example for a valid newer JSON version:

```json
{
	"type": "MULTICOLUMN",
	"hideOnMobile" : false,
	"hideOnDesktop" : false,
	"stacking": "left-on-top",
	"background":{
		"image":{
			"src":"https://example.png",
			"repeat":"repeat-y",
			"position":"center top"
		},
		"color":"#ECC9C9"
	},
	"children": [
		{
			"type": "COL_SPACER",
			"width": 10,
			"height": 10
		},
		{
			"type": "COLUMN",
			"width": 35,
			"children": [
				{
					...
				}
			]
		},
		{
			"type": "COL_SPACER",
			"width": 10,
			"height": 10
		},
		{
			"type": "COLUMN",
			"width": 35,
			"background":{
				"image":{
					"src":"",
					"repeat":"repeat-y",
					"position":"center top"
				},
			"color":"#ECC9C9"
			},
			"children": [
				{
					...
				}
			]
		},
		{
			"type": "COL_SPACER",
			"width": 10,
			"height": 10
		}
	]
}
```
Detailed property table for the older version:

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| hideOnMobile |  | boolean | if it set to `true`, the multi-column won't show on mobile view |
| hideOnMobile |  | boolean | if it set to `true`, the multi-column won't show on desktop view |
| reorderOnMobile |  | boolean | if this property is set to `true`, the columns inside the multi-columns will stack on top of each other in mobile view|
| cols | array | | The cols array may contain the child elements of the columns|
children | array |  | The children array may [contain any of our element types](/elements) except the fullwidth element. |
| children.hideOnMobile |  | boolean | if it's set to `true`, the column won't show on mobile view |
children.lock |  |boolean | It's a Chamaileon editor related property, if it's set to `true`, the column's width will remain the same even if the user adds more columns
children.width | number | percentage | It's used to define the width relative to the child element's parent object

Detailed property table for the newer version:

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| hideOnMobile |  | boolean | if it set to `true`, the multi-column won't show on mobile view |
| hideOnMobile |  | boolean | if it set to `true`, the multi-column won't show on desktop view |
| stacking | string | "left-on-top", "right-on-top", "none" | it is a custom property that can define the order which the cells are going to stack |
background | object | object | [Read more](/property-groups/background/README.md)
| children | array | | The children array may contain column and column spacer elements |
| children.col_spacer | string | "COL_SPACER" | sets the column's type to spacer (it's a column without any content, used to control the layout) |
children.width | number | integer | The JSON contains this value as the width relative t the parent element in percentage value, but the generator creates a pixel value from it. |
children.height | number | integer | The generator only accepts the height property defined as a number and generates a fixed value from it in pixels. |
children.column | array |  | This array contains the child elements of one column
children.width | number | integer | The JSON contains this value as the width relative t the parent element in percentage value, but the generator creates a pixel value from it. |
children | array |  | The children array may [contain any of our element types](/elements) except the fullwidth element. |
| children.hideOnMobile |  | boolean | if it's set to `true`, the column won't show on mobile view |

Note: The `stacking` property is one of the new properties and it alternates the `reorderOnMobile` property. If `reorderOnMobile` is set to `true`, the child elements of the columns are stacking on top of each other, always starting with the first left column. If it set to `false`, the columns are going to scale down to fit to the mobile screen.
The main difference is that now you can control the direction of the stacking with the usage of `stacking` instead of the `reorderOnMobile` parameter.
