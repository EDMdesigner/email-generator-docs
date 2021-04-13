# Template languages


This generator setting is used to set the template language for the `conditional` and `loop` elements. 

Currently supported template languages: `handlebars, liquid, mustache`.

For more information you can visit:

If you are using Handlebars: https://sendgrid.com/docs/for-developers/sending-email/using-handlebars/#conditional-statements

If you are using Liquid: https://shopify.github.io/liquid/tags/control-flow/

If you are using Mustache: https://mustache.github.io/mustache.5.html


Default value:
```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"templatingLanguage": "handlebars",
		...
	}
}