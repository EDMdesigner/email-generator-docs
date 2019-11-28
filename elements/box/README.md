The `box` element can contain all the another elements except the `full width` element. The primary function of the `box` element is wrapping its children elements with a HTML table structure because some of the CSS rules only apply on `<table>` or `<td>` elements (mostly on Outlooks). This HTML table stucture help in grouping elements, for example apply one background image behind a text and a button element.

This wrapper table helps:
- positioning its children elements inside the email layout
- apply padding, margin, border and background setting around different element or group of elements
- added class attributes take place on the wrapper table on the proper level (`<table>` or `<td>`)


Example JSON:
```
{
    "type":"BOX",
    "children":[
        ...
    ],
    "background":{
        ...
    },
    "border":{
        ...
    },
    "margin":{
        ...
    },
    "padding":{
        ...
    },
    "hideOnDesktop":false,
    "hideOnMobile":false
    }
```
Properties | Type | Values | Description
--- | --- | --- | ---
children | array |  | The children array may [contain any of our element types](../elements) except the full-width element.
background | object | object | [Read more](../prop-groups/background.md)
border | object | object | [Read more](../prop-groups/border.md)
margin | object | object | [Read more](../prop-groups/margin.md)
padding | object | object | [Read more](../prop-groups/margin.md)
hideOnDesktop |  | boolean | If it set to `true`, the generator add a class to the box element table to hide the content on desktop
hideOnMobile |  | boolean | If it set to `true`, the generator add a class to the box element table to hide the content on mobile 