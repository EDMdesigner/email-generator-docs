# Generator modes

You can use our generator with different output formats that are named modes. These have a different html structure and it's target clients differ as well.
Currently we have 4 modes: `classic, div-only, table-desktop, hybrid`.

You can read more about these modes [here](https://add-link) TODO: replace this

Default value:

```json
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document": { ... },
	"settings": {
		"generatorMode": "classic",
		...
	}
}
```

**The supported generator options differ between the modes as well.**

Div-only

```json
{
	"settings": {
		"encodeUrls": true,
		"previewTextHack": false,
		"lineLength": 799,
		"forceHexaColors": true,
		"templatingLanguage": "handlebars",
		"generatorMode": "div-only",
		"lang": "en",
		"useFullwidthMarker": false,
	}
}
```



Classic, Table-desktop, Hybrid
```json
{
	"settings": {
		"vmlBackground": true,
		"rolePresentation": false,
		"encodeUrls": true,
		"previewTextHack": false,
		"lineLength": 799,
		"buttonType": "classic",
		"forceHexaColors": true,
		"templatingLanguage": "handlebars",
		"generatorMode": "table-desktop",
		"lang": "en",
		"useFullwidthMarker": false,
	}
}
```
