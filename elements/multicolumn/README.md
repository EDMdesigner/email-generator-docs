Multicolumns are the main elements to create complex layouts. They can have multiple columns and every column has a children array that contains the properties of the content. The children array of the columns can contain every element except the full width container. [Read more](//fullwidth_container/README.md)

The arrays in the “cols” array represent the columns. The minimum number of columns is 2 and it can be grown to as many as you need. We support max. 5 in our EDMdesigner editor, but there is no limitation built in the generator.

The columns can't have padding, margin and border properties, these properties need to be added to the elements inside the children array. [Read more on set these properies](../../property-groups)

There are new features in the generator, now it is possible to:
 - set background properties to the multicolumn and/or the columns. (Keep in mind if generating `VML background` is set to `true` and you set background image on both elements, on Outlook email clients only the multicolumns image will appearing. [Read more on VML background](../../generator-settings/VMLbackground.md)
  - define a child element called `COL_SPACER` and with its `width` and `height` propery set a spacing around the columns inside the multicolumns. (It creates a more predictable and unified layout across various email clients)

The width of the multicolumn is set to 100% and extends to the full width of its parent element. The width of the child elements of the columns is calculated from the width of the multicolumns parent elements width.

Keep in mind that: 
 - the sum of the child elements width (if the column contains an element with padding, margin and/or border width set on, these are count in too) won't exceed the parent elements width, because the last column might break into a new line. It applies to the column spacings too, the sum of the columns and column spacings width might not pass 100%.
 - too long words in a paragraph might push out the width of the column that result in breaking the layout.

Example for a valid older JSON version:

```
{
	"type" : "MULTICOLUMN",
	"hideOnMobile" : false,
	"hideOnDesktop" : false,
	"stacking": "left-on-top",
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

```
{
	"type": "MULTICOLUMN",
	"hideOnMobile" : false,
	"hideOnDesktop" : false,
	"reorderOnMobile": true,
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
Detailed propery table for the older version:

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on mobile view |
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on desktop view |
| reorderOnMobile |  | boolean | if this propery is set to `true`, the columns inside the multicoluns are stacking on top of each other in mobile view|
| cols | array | | The cols array may contain the child elements of the columns|
children | array |  | The children array may [contain any of our element types](/elements) except the full-width element. |
| children.hideOnMobile |  | boolean | if it set to `true`, the column won't show on mobile view |
children.lock |  |boolean | It's a chamaileon editor related property, if it set to `true`, the column's width remain the same even if the user add more columns
children.width | number | percentage | It is used to define the width as relative to the child elements's parent object

Detailed propery table for the newer version:

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on mobile view |
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on desktop view |
| stacking | string | "left-on-top", "right-on-top", "none" | it is a custom propery to set the direction of the stacking of the columns on top of each other |
background | object | object | [Read more](/property-groups/background/README.md)
| children | array | | The children array may contain column and spacer column elements |
| children.col_spacer | string | "COL_SPACER" | set the colunms type to spacer (it's a column without any content, used to control the layout) |
children.width | number | integer | The JSON contain this value as the width compared of the parent element express in percentage, but the generator generates a fixed value expressed as px from it. |
children.height | number | integer | The generator only accept the height property defined in number and generates a fixed value expressed as px. |
children.column | array |  | This array contains the child elements of one column
children.width | number | integer | The JSON contain this value as the width compared of the parent element express in percentage, but the generator generates a fixed value expressed as px from it. | 
children | array |  | The children array may [contain any of our element types](/elements) except the full-width element. |
| children.hideOnMobile |  | boolean | if it set to `true`, the column won't show on mobile view |

Note: The `stacking` property is one of the new properties and it alternates the `reorderOnMobile` property. If `reorderOnMobile` is set to `true`, the child elements of the columns are stacking on top of each other, always start with the first left column. If it set to `false`, the columns are scaling down to fit to the mobile screen.
 The main difference is now you can control the direction of the stacking with using the `stacking` instead of the `reorderOnMobile`.