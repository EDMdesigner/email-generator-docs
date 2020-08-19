The loop element only have 2 properties: expression and children.
Depending on your expression, it can loop through your data to build lists for example.
You can choose the templating language that you would like to use in tha email properties settings, which can be reached throught the toolbox too.

For more information you can visit:

If you are using Handlebars: https://sendgrid.com/docs/for-developers/sending-email/using-handlebars/#iterations

If you are using Liquid: https://shopify.github.io/liquid/tags/iteration/

If you are using Mustache: https://mustache.github.io/mustache.5.html

```
{
	"type" : "LOOP",
	"expression": "user.orderHistory",
    "children":[
        ...
    ]
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
expression | string | must be a valid expression
children | array | The children array may [contain any of our element types](/elements) except the full-width element.

