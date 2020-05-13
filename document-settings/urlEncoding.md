URL Encoding converts reserved, unsafe, and non-ASCII characters in URLs to a format that is universally accepted and understood by web browsers and servers. It first converts the character to one or more bytes. Then each byte is represented by two hexadecimal digits preceded by a percent sign.

In the generator there is a built in encoder that handles malformatted or decoded reserved characters, like ?, /, #, :. However it can turned off, because some ESP's use a similar method (it unnecessary to do this twice) or if you use one of our editor and use merge tags, those need to be intact and handled by your ESPs later.

Inside the settings object you can now place a `encodeUrls` parameter either of the values true or false:

-If it set to `true`, the generator will encode the escape characters in the HTML

-If it set to `false`, the generator won't make any changes on the format

Example JSON:

```
{

	"document: { ... },
	"settings": {
		"encodeUrls": true,
		...
	}
}
```