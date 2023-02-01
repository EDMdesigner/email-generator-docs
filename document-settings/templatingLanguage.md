# Template languages


This generator setting is used to set the template language for the `conditional` and `loop` elements.

Currently supported template languages: `handlebars, liquid, mustache, mailchimp, acc`.

For more information you can visit:

If you are using Handlebars: https://sendgrid.com/docs/for-developers/sending-email/using-handlebars/#conditional-statements

If you are using Liquid: https://shopify.github.io/liquid/tags/control-flow/

If you are using Mustache: https://mustache.github.io/mustache.5.html

If you are using Mailchimp: https://mailchimp.com/help/use-conditional-merge-tag-blocks/

If you are using Adobe Campaign Classic (acc): https://experienceleague.adobe.com/docs/campaign-classic/using/sending-messages/personalizing-deliveries/conditional-content.html?lang=en

*Note: Mailchimp has no loop merge tag so we're using handlebars as a fallback for it*

Default value:
```json
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document": { ... },
	"settings": {
		"templatingLanguage": "handlebars",
		...
	}
}
