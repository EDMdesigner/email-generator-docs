The border area, bounded by the border edge, extends the padding area to include the element's borders. The border properties specify the width, color, and style of the border area of a box. [Read more](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

The generator can handle border settings in various types of elements. The border property group is used in the following types:
 - [box](../../elements/box/README.md)
 - [divider](../../elements/divider/README.md)
 - [multicolumn](../../elements/multicolumn/README.md)
 - [image](../../elements/divider/README.md)
 - [button](../../elements/button/README.md)

```
    "border" : {
        "top" : {
            "color" : "#0E4857",
            "width" : 5,
            "style" : "solid"
        },
        "right" : {
            "color" : "#0E4857",
            "width" : 5,
            "style" : "solid"
        },
        "bottom" : {
            "color" : "#0E4857",
            "width" : 5,
            "style" : "solid"
        },
        "left" : {
            "color" : "#0E4857",
            "width" : 5,
            "style" : "solid"
        },
        "radius" : 5
```

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| border.top | object | object |
| border.top.color | string | hex code | 6 digit hex codes have the most extensive support across email clients
| border.top.width | number | integer | The generator only accept the border-width defined in number and generates a fixed value expressed as px. [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)
| border.top.style | string | none, hidden, dotted, dashed, solid, double ... | [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-style)
| border.right | object | object |
| border.right.color | string | hex code | 6 digit hex codes have the most extensive support across email clients
| border.right.width | number | integer | The generator only accept the border-width defined in number and generates a fixed value expressed as px. [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-width)
|border.right.style | string | none, hidden, dotted, dashed, solid, double ... | [more about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-style)
| border.bottom | object |object |
| border.bottom.color | string | hex code | 6 digit hex codes have the most extensive support across email clients
| border.bottom.width | number | integer | The generator only accept the border-width defined in number and generates a fixed value expressed as px. [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-width)
| border.bottom.style | string | none, hidden, dotted, dashed, solid, double ... | [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-style)
| border.left | object |object |
| border.left.color | string | hex code | 6 digit hex codes have the most extensive support across email clients
| border.left.width | number | integer | The generator only accept the border-width defined in number and generates a fixed value expressed as px. [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-width)
| border.left.style | string | none, hidden, dotted, dashed, solid, double ... | [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-style)
| border.radius | number | integer | [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

