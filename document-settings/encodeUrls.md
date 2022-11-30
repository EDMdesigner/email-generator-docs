# URL encoding

URL Encoding converts reserved, unsafe, and non-ASCII characters in URLs to a format that is universally accepted and understood by web browsers and servers. It first converts the character to one or more bytes. Then each byte is represented by two hexadecimal digits preceded by a percent sign.

In the generator there is a built in encoder that handles malformatted or decoded reserved characters, like ?, /, #, :. However it can be turned off, because some ESP's use a similar method (it is unnecessary to do this twice).


If you are using merge tags and the output is malformatted then you should consider turning this feature off. There is a fixer method added to this encoder that should turn most of the merge tags back to their original form but it's not flawless and can miss some merge tag styles.

Inside the settings object you can now place a `encodeUrl`'s parameter either of the values true or false:

-If it set to `true`, the generator will encode the escaped characters in the HTML

-If it set to `false`, the generator won't make any changes on the format

Example JSON:

```json
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"encodeUrls": true,
		...
	}
}
```
