# Divider element

The divider is technically an “empty box” which can have the spacing, background, and lineStyle properties. The primary function of this leaf element is to separate the content into smaller logical blocks.

```json
{
	"type" : "DIVIDER",
	"align" : "center",
	"lineStyle" : {
		"color" : "#60d335",
		"width" : 4,
		"style" : "solid"
	},
	"spacing" : {
		"top" : 10,
		"right" : 10,
		"bottom" : 10,
		"left" : 10
	},
	"width" : 100,
	"transparent" : false,
	"lastDividerColor" : null,
	"background" : {
		...
	},
}
```
Properties | Type | Values | Description
--- | --- | --- | ---
align | string | left, center, right | set the position of the divider inside its parent container
background | object | object | [Read more](../prop-groups/background.md)
lineStyle | object | object |
lineStyle.color| string | hex code | set the color of the divider line
lineStyle.width | number | integer | set the thickness of the divider line
lineStyle.style | string | solid, dotted etc. | it can have the same values like the border style: [more about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
spacing | object | object |
width | number | percentage | It is used to define the width as to the parent element's width
transparent |  | boolean | if it set to `true` the line will become transparent and the element becomes more like a spacer
lastDividerColor |  |  | editor related property (it is not necessary)
