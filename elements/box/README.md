# Box element

The `box` element can contain all the another elements except the `fullwidth` element. The primary function of the `box` element is wrapping its children elements with a HTML table structure because some of the CSS rules only apply on `<table>` or `<td>` elements (mostly on Outlooks). This HTML table structure helps in grouping elements, for example apply one background image behind a text and a button element.

This wrapper table helps:
- positioning its children elements inside the email layout
- applying padding, margin, border and background settings around different elements or group of elements
- adds class attributes that take place on the wrapper table on the proper level (`<table>` or `<td>`)

Example JSON:
```json
{
    "type":"BOX",
    "hideOnDesktop":false,
    "hideOnMobile":false,
    "margin":{
        ...
    },
    "border":{
        ...
    },
    "padding":{
        ...
    },
    "background":{
        ...
    },
    "children":[
        ...
    ]
}
```
Properties | Type | Values | Description
--- | --- | --- | ---
hideOnDesktop |  | boolean | If it's set to `true`, the generator adds a class to the box element table to hide the content on desktop
hideOnMobile |  | boolean | If it's set to `true`, the generator adds a class to the box element table to hide the content on mobile
margin | object | object | [Read more](/property-groups/margin/README.md)
border | object | object | [Read more](/property-groups/border/README.md)
padding | object | object | [Read more](/property-groups/padding/README.md)
background | object | object | [Read more](/property-groups/background/README.md)
children | array |  | The children array may [contain any of our element types](/elements) except the fullwidth element.
