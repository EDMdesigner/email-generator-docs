description

Example JSON:
```
{
    "background":{
    "image":{
        "src":"https://examples/example.png"
        "position":"center center",
        "repeat":"no-repeat",

    },
    "color":"#60DE55"
    }
}
```
| Properties | Type | Values | Description |
| --- | --- | --- | ---
| color | string  | hex code | hex codes have better support amongst email clients, than RGBa |
| image | object |  |  |
| image.src | string | URL |  |
| image.repeat | string | repeat, repeat-x, repeat-y, no-repeat |  |
| image.position | string | top, left, center, bottom, right | [read more](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)|


The background property group is used in the following types:
 - [BOX](../elements/box.md)
 - [FULLWIDTH](../elements/fullwidth.md)
 - [BODY](../elements/body.md)

 Note: [Read more on background usage](../generator-settings/VMLbackground.md)