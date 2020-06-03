About how to set the appearance of the button you can find more information [here](/elements/button/README.md).

 In our editor there is an `email properties` option where you can change the generator's behavior on how to generate the code of the button by change the `buttonType` propery. You can choose that you need a fully clickable button or disable it.
 When this setting is enabled, the software generates fully-clickable buttons for modern email clients and simple fallback buttons for Outlooks. Some ESPs might not be able to handle this code properly, so if you experience any issues, just disable this switch and the software will generate classic buttons in which only the text is clickable.

In the JSON file it is defined by two string values, `classic` or `minimal`.

Inside the `settings` object you can now place a `buttonType` parameter with the following values:

-If it set to `classic`, the generator will place the button code inside conditional comments and will generate a fully clickable button that supported most of the email clients and a fallback button for Word based Outlook clients.**

-If it set to `minimal`, the generator will set only the fallback button, that has the same appearance, however only the text of the button will be clickable.

Example JSON:

```
{

	"document: { ... },
	"settings": {
		"buttonType": "classic",
		...
	}
}
```

** Some ESP won't support this fallback mechanism and even rip off conditional comments, that can cause the duplications or delete the button code entirely. Testing the generated code used first time is highly recommended and the ESP made any changes on the button code, use the `minimal` button code instead.

