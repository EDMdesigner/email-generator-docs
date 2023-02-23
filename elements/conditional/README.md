# Conditional element

The conditional element only has 2 properties: expression and children.
Depending on your expression, it can show/hide it's children.
You can choose the template language that you would like to use in the email properties settings, which can be reached through the toolbox too.

For more information you can visit:

If you are using Handlebars: https://sendgrid.com/docs/for-developers/sending-email/using-handlebars/#conditional-statements

If you are using Liquid: https://shopify.github.io/liquid/tags/control-flow/

If you are using Mustache: https://mustache.github.io/mustache.5.html

If you are using Mailchimp: https://mailchimp.com/help/use-conditional-merge-tag-blocks/

If you are using Adobe Campaign Classic (acc): https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/conditional-content.html?lang=en

```json
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
children | array | The children array may [contain any of our element types](/elements) except the fullwidth element.

