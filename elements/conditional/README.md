The conditional element only have 2 properties: expression and children.
Depending on your expression, it can show/hide it's children.
You can choose the templating language that you would like to use in the email properties settings, which can be reached throught the toolbox too.

For more information you can visit:

If you are using Handlebars: https://sendgrid.com/docs/for-developers/sending-email/using-handlebars/#conditional-statements

If you are using Liquid: https://shopify.github.io/liquid/tags/control-flow/

If you are using Mustache: https://mustache.github.io/mustache.5.html

```
{
	"type" : "CONDITIONAL",
	"expression": "user.profile.male",
	"children":[
		...
	]
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
expression | string | must be a valid expression
children | array | The children array may [contain any of our element types](/elements) except the full-width element.

