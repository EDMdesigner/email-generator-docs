Multicolumns are the main elements to create complex layouts. They can have multiple columns (we support max. 5 in our editor) and every columns can have children. The children array can contain every element except the full width container. [Read more](//fullwidth_container/README.md)

The arrays in the “cols” array represent the columns. The minimum number of columns is 2 and it can be grown to 5.

The columns can't have padding, margin, background and border properties, these properties need to be added to the elements inside the children array. 

The width of the multicolumn is set to 100% and extends to the full width of its parent element. The width of the columns is calculated from the width of the multicolumns parent elements width.
Keep in mind that: 
 - the sum of the child elements width (with the padding, margin and border width values) won't exceed the parent elements width, because the last column might break into a new line
 - too long words in a paragraph might push out the width of the column that result in breaking the layout

```
{
	"type" : "MULTICOLUMN",
	"hideOnMobile" : false,
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
| hideOnMobile | string  | boolean | if it set to `true`, the multicolumn won't show on mobile view |
| stacking | string | "left-on-top", "right-on-top", "none" | it is a custom propery to set the direction of the stacking of the columns on top of each other |
| cols | array | | The cols array may contain children elements |
children | array |  | The children array may [contain any of our element types](/elements) except the full-width element. |
| children.hideOnMobile | string  | boolean | if it set to `true`, the column won't show on mobile view |
children.lock | string | boolean | It's a chamaileon editor related property, if it set to `true`, the column's width remain the same even if the user add more columns
children.width | number | percentage | It is used to define the width as relative to the child elements's parent object