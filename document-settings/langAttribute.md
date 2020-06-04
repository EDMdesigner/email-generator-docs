There is now possible to change the value of the language attribute on the html tag to declare the default language of the text in the email. The default value is english and the generator will fallback to this if it is not been defined otherwise.

Defining this attribute is good for both accessibility reasons and the HTML has less chance to fail in any built in validation process.

You can find more information and the list of the subtags [here](https://www.w3.org/International/articles/language-tags/).

Example JSON:

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"lang": "fr",
		...
	}
}
```
