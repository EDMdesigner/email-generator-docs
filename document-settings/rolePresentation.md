Our generator uses tables for controlling the layout, mostly because some of the email clients not support padding and margin styling on `div` tags.
[You can find more information about this here](https://blog.edmdesigner.com/html-email-padding-margin-border/)

For **accessibility** reasons, we built in the generator a new setting, called rolePresentation. It adds a `presentation` role to the table that used for layout purposes. 
It removes any semantic meaning from the table element and any of its table related children elements, such as table headers and table data elements. Non-table related elements should retain their semantic meaning, however. This way screenreaders can recognise that how to interpret these tables.
[More on tis topic](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_presentation_role)

Inside the settings object you can now place a rolePresentation parameter either of the values true or false:

-If it set to `true`, the generator will add `role="presentation"` attribute to every table tag. 

-If it set to `false`, the generator only generate the tables' default attributes that necessary to avoid mayor layout flaws, like unwanted borders on table cells.

The default setting is:

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"rolePresentation": false,
		...
	}
}
```

Note: Keep in mind that using this role setting can increase the size of the generated HTML code, especially for complex email layouts.