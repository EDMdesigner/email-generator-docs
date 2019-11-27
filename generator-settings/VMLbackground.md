
VML is stands for Vector Markup language and this format is used for define shapes that renders correctly on Word engined Outlook versions. From Outlook2007 to the newest versions, Outlooks only render the background images or the rounded shape buttons if they were declared in VML.

Inside the settings object you can now place a vmlBackground parameter either of the values true or false:

-If it set to `true`, the generator will generate declarations for the background in HTML and VML as well. VML code will be placed inside coditional comments to ensure that only Outlook email clients notice that.

-If it set to `false`, the generator only generate the HTML. This setting option only recommended if your target audience does not contain Outlook email client users.

The default setting is:

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"vmlBackground": true,
        ...
	}
}
```

[Example JSON file](../email-generator-docs/full-email-layout-examples)

Note: if you choose VML background, only use one image, do not use more background images overlayed on each other. VML backgrounds can't be nested inside each other -because of their built in rendering logic- therefore the generator will rendering only the closest parent element's background image.
