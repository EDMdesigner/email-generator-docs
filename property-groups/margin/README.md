# Margin property

By definition margins create an extra space around an element. Because margins -like paddings- can be handled differently across email clients, there are workarounds to solve typical issues. [Read more](https://blog.edmdesigner.com/html-email-padding-margin-border/)

Even though in the JSON file the values of the margin are stored called as `margin`, it's interpreted a bit different. If a [box](/elements/box/README.md) element has margin values as well, the generator wraps the whole element in an another wrapper table and applies the values as padding. This method makes it possible to avoid possible issues that effect the usage of margins.

Example JSON:
```json
{
    "margin":{
        "top":10,
        "right":15,
        "bottom":20,
        "left":15
    }
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
margin | object | object |
margin.top | number | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)
margin.right | number | integer| [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
margin.bottom| number | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)
margin.left | number | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)

Note: The margin property can be defined by negative numbers or the value `auto`, but the generator can't handle these values because of these value's poor email client support. Negative margin values are not supported on some of the mayor email clients, like Gmail, Outlook 2007-2019, Outlook.com.
