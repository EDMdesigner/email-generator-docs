# Loop element

The loop element only has 2 properties: expression and children.
Depending on your expression, it can loop through your data (for example: to build lists).
You can choose the template language that you would like to use in the email properties settings, which can be reached through the toolbox too.

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
children | array | The children array may [contain any of our element types](/elements) except the fullwidth element.

