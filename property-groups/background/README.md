# Background property

Using background color and images really can add to the look of an email. There are a lot of practices on how to use background to improve the look of an email:
- place repeating patterns around the email content
- highlighting the most important part of a content with an eye-catching background color or image behind it

The generator can handle background settings in various types of elements. The background property group is used in the following types:
 - [box](../../elements/box/README.md)
 - [fullwidth elelment](../../elements/fullwidth/README.md)
 - [body](../../elements/body/README.md)
 - [text](../../elements/text/README.md)
 - [multi-column](../../elements/multicolumn/README.md)
 
Between the generator settings there is an option that can set the generator to create the definition of the background in Vector Markup Language too. This block of code is only necessary for Outlooks on Windows.
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


 Note: Not all the email clients support background image, keep in mind that always set a fallback background color and the image should only as a decoration.