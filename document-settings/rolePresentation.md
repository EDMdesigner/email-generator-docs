# Presentation role for tables

Our generator uses tables for controlling the layout, mostly because some of the email clients doesn not support padding and margin styling on `div` tags.
[You can find more information about this here](https://blog.edmdesigner.com/html-email-padding-margin-border/)

For **accessibility** reasons, we added a new setting in the generator called rolePresentation. It adds a `presentation` role to the table that is used for layout purposes.
It removes any semantic meaning from the table element and any of it's table related children elements, such as table headers and table data elements. However non-table related elements should retain their semantic meaning. This way screen readers can interpret these tables correctly.
[More on tis topic](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_presentation_role)

Inside the settings object you can now place a rolePresentation parameter with a value of true or false:

-If it set to `true`, the generator will add a `role="presentation"` attribute to every table tag.

-If it set to `false`, the generator will only generate the table's default attributes that are necessary to avoid mayor layout flaws, like unwanted borders on table cells.

The default setting is:

```json
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
