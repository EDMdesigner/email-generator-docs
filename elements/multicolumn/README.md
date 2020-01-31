Multicolumns are the main elements to create complex layouts. They can have multiple columns and every column has a children array that contains the properties of the content. The children array of the columns can contain every element except the full width container. [Read more](//fullwidth_container/README.md)

The arrays in the “cols” array represent the columns. The minimum number of columns is 2 and it can be grown to as many as you need. We support max. 5 in our EDMdesigner editor, but there is no limitation built in the generator.

The columns can't have padding, margin, background and border properties, these properties need to be added to the elements inside the children array. 

The width of the multicolumn is set to 100% and extends to the full width of its parent element. The width of the child elements of the columns is calculated from the width of the multicolumns parent elements width.
Keep in mind that: 
 - the sum of the child elements width (with the padding, margin and border width values) won't exceed the parent elements width, because the last column might break into a new line
 - too long words in a paragraph might push out the width of the column that result in breaking the layout

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

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on mobile view |
| hideOnMobile |  | boolean | if it set to `true`, the multicolumn won't show on desktop view |
| stacking | string | "left-on-top", "right-on-top", "none" | it is a custom propery to set the direction of the stacking of the columns on top of each other |
| cols | array | | The cols array may contain children elements |
children | array |  | The children array may [contain any of our element types](/elements) except the full-width element. |
| children.hideOnMobile |  | boolean | if it set to `true`, the column won't show on mobile view |
children.lock |  |boolean | It's a chamaileon editor related property, if it set to `true`, the column's width remain the same even if the user add more columns
children.width | number | percentage | It is used to define the width as relative to the child elements's parent object

Note: The `stacking` property is one of the new properties and it alternates the `reorderOnMobile` property. If `reorderOnMobile` is set to `true`, the child elements of the columns are stacking on top of each other, always start with the first left column. If it set to `false`, the columns are scaling down to fit to the mobile screen.
 The main difference is now you can control the direction of the stacking with using the `stacking` instead of the `reorderOnMobile`.