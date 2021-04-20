# Padding property

An element's padding area is the space between its content and its border. It creates an extra space within the element. As usual, different email clients have different ways to handle spacing around and between elements ([Read more](https://blog.edmdesigner.com/html-email-padding-margin-border/#testingmarginspaddingsandborders)). For example Outlook doesn’t acknowledge `<div>`s or their padding attributes.

The most supported approach to get the same results on every email client is wrapping all the elements inside a table and applying the padding only on the `<td>`. [Read more](https://blog.edmdesigner.com/html-email-padding-margin-border/#testingmarginspaddingsandbordersontablewrappers)

To get more information about how the generator handles the padding on different elements, check out the description of the [box](/elements/box/README.md) element.


Example JSON:
```
    "padding":{
        "top":10,
        "right":15,
        "bottom":20,
        "left":15
    }
```

Properties | Type | Values | Description
--- | --- | --- | ---
padding | object | object | 
padding.top | number | integer |[Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-top)
padding.right | number | integer |[Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-right)
padding.bottom| number | integer |[Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-bottom)
padding.left | number | integer |[Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-left)