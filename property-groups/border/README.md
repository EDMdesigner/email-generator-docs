# Border property

The border area, bounded by the border edge, extends the padding area to include the element's borders. The border properties specify the width, color, and style of the border area of a box. [Read more](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

The generator can handle border settings in various types of elements. The border property group is used in the following types:
 - [box](../../elements/box/README.md)
 - [divider](../../elements/divider/README.md)
 - [multi-column](../../elements/multicolumn/README.md)
 - [image](../../elements/divider/README.md)
 - [button](../../elements/button/README.md)

```json
{
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
}
```

| Properties | Type | Values | Description |
| --- | --- | --- | ---
| border.* | object | object |
| border.*.color | string | hex code | 6 digit hex codes have the most extensive support across email clients
| border.*.width | number | integer | The generator only accepts the border-width defined as a number and generates a fixed value expressed in pixels. [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)
| border.*.style | string | none, hidden, dotted, dashed, solid, double ... | [More about the values](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-style)


*= top, right, bottom, left

