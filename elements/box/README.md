The `box` element can contain all the another elements except the `full width` element. The primary function of the `box` element is wrapping its children elements with a HTML table structure because some of the CSS rules only apply on `<table>` or `<td>` elements (mostly on Outlooks).

This wrapper table helps:
- positioning its children elements inside the email layout
- apply padding, margin, border and background setting around different element
- added class attributes take place on the wrapper table on the proper level (`<table>` or `<td>`)


Example:
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
| Properties    | Type          | Values | Description
| ------------- |:-------------:| -----:|
| background | object | object | [Read more](../prop-groups/background.md)
| children | array |  | The children array may [contain any of our element types](../elements) except the full-width element.
| border | object | object | [Read more](../prop-groups/border.md)
| padding | object | object | 