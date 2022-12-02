# Set the buttonType

In the `settings` there is a `buttonType` option where you can change the generator's behavior on how to generate the code of the button. You can choose that you need a fully clickable button with a slightly complex fallback mechanism or a more simple button with only the text clickable.

In the JSON file it is defined by two string values, `classic` or `minimal`.

Inside the `settings` object you can now place a `buttonType` parameter with the following values:

- If it's set to `classic`, the generator will place the button code inside conditional comments and will generate a fully clickable button that is supported by most of the email clients and a fallback button for Word based Outlook clients.**

- If it's set to `minimal`, the generator will set only the fallback button, that has the same appearance, however only the text of the button will be clickable.

Example JSON:

```json
{

	"document": { ... },
	"settings": {
		"buttonType": "classic",
		...
	}
}
```

About how to set the appearance of the button you can find more information [here](/elements/button/README.md).

** Some ESP won't support this fallback mechanism and even rip off conditional comments, that can cause the duplications or delete the button code entirely. Testing the generated code first is highly recommended and if the ESP made any changes on the button code, use the `minimal` button code instead.

If you have any questions or you notice any issues while using our exported code, feel free to create an issue [here](https://github.com/EDMdesigner/email-generator-docs/issues).

