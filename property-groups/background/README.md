Background images are images that are applied to the background of an element in an email. The main difference compared with a hero image is that you can place HTML content on top of them. 

[Read more on  VML background usage](../generator-settings/VMLbackground.md)
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

 Note: Not all the email clients support background image, keep in mind that always set fallback background color and the image has to serve only decorational purpose.  