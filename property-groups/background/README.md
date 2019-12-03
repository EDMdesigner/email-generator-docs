Using background color and images really can add to the look of an email. There are a lot of practices on how to use background to improve the look of an email:
- place repeating pattern around the email content
- highlighting the most important part of a content with eye-catching background color or image behind it

The generator can handle background settings in various types of elements. The background property group is used in the following types:
 - [BOX](../elements/box.md)
 - [FULLWIDTH](../elements/fullwidth.md)
 - [BODY](../elements/body.md)
 
Between the generator settings there is an option to choose that the generator make the definition of the background in Vector Markup Language too. This block of code is only necessary for Outlooks on Windows.
[Read more on VML background usage](../../generator-settings/VMLbackground.md)

Example JSON:
```
{
    "color":"#60DE55",
    "image":{
        "src":"https://examples/example.png"
        "repeat":"no-repeat",
        "position":"center center"
    }
}
```
| Properties | Type | Values | Description |
| --- | --- | --- | ---
| color | string  | hex code | hex codes have better support amongst email clients, than RGBa |
| image.src | string | URL |  |
| image.repeat | string | repeat, repeat-x, repeat-y, no-repeat | [read more](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat) |
| image.position | string | [read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position) | [read more](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)|


 Note: Not all the email clients support background image, keep in mind that always set fallback background color and the image has to serve only decorational purpose.