By definition margins create extra space around an element. Because margins -like paddings- 
can be handled differently across email clients, there are workarounds to solve typical issues. [Read more](https://blog.edmdesigner.com/html-email-padding-margin-border/)

Even though in the JSON file the values of the margin are stored called as `margin`, it inerpretended a bit different. If a [box](/elements/box/README.md) element have magin values as well, the generator wraps the whole element another wrapper table and apply the values as padding. This method make possible to avoid possible issues that effect using margin property.

Example JSON:
```
    "margin":{
        "top":10,
        "right":15,
        "bottom":20,
        "left":15
    }
```

Properties | Type | Values | Description
--- | --- | --- | ---
margin | object | object |
margin.top | | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
margin.right | | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
margin.bottom| | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
margin.left | | integer | [Read about the list of values](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)