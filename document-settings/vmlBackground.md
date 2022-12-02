# Vml background

VML stands for Vector Markup language and this format is used for define shapes that are rendered correctly on Outlook versions using the Word rendering engine. From Outlook 2007 to the newest versions, Outlook only renders the background images or the rounded shape buttons if they are declared in VML.

Inside the settings object you can now place a vmlBackground parameter either of the values true or false:

- If it's set to `true`, the generator will generate declarations for the background in HTML and in VML as well. VML code will be placed inside conditional comments to ensure that only Outlook email clients will notice it.

- If it's set to `false`, the generator will only generate the HTML. This setting option is only recommended if your target audience does not contain users that use Outlook email clients.

The default setting is:

```json
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document": { ... },
	"settings": {
		"vmlBackground": true,
		...
	}
}
```

[Example JSON file](../full-email-layout-examples/vml_background_example.json)

Note: if you use this setting, only use one image, do not use more background images overlaying on each other. VML backgrounds can't be nested inside each other - because of their built in rendering logic - therefore the generator will render only the background closest to the parent element.
