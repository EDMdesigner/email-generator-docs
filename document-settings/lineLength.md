# Line length

If you make an email HTML, there is a limit on the number of characters in a line. It is possible to minify your code into one line, but some email clients may have trouble parsing it and that can cause a lot of issues.
For example if a transfer agent or email client receives the HTML code with longer lines than the length it can handle, then the line will be broken. As the client moves through the code it can break the line at an arbitrary point. If that break happens in the middle of an HTML tag, it could make the tag unreadable. From that point various kinds of rendering issues can occur, mostly display errors that can affect the whole layout. Because of this most ESPs have their own validation logic to check the length of lines and forbid using longer lines than the acceptable amount of characters.

The optional number of characters in a line are **less, than 1000 characters**.
[Read more](https://tools.ietf.org/html/rfc2822#section-2.1.1)

Inside the settings object you can place a lineLength parameter, the value can be an integer number. With this setting you'll get more control over how to parse the HTML code without using a third party tool.

The default setting is:

```json
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document": { ... },
	"settings": {
		"lineLength": 799,
		...
	}
}
```
Note: If your ESP does not have a special recommendation to the length of lines, the default setting is a safe bet, there is no need to change it.
