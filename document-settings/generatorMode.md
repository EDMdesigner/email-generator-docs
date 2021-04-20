# Generator modes

You can use our generator with different output formats that are named modes. These have a different html structure and it's target clients differ as well.
Currently we have 4 modes: `classic, div-only, table-desktop, hybrid`.

You can read more about these modes [here](https://add-link) TODO: replace this

Default value:

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		"generatorMode": "classic",
		...
	}
}
```

**The supported generator options differ between the modes as well.**

Div-only

```
"settings": {
	{
		encodeUrls: true,
		lang: "en",
		lineLength: 799,
		templatingLanguage: "handlebars",
		generatorMode: "table-desktop",
	}
}
```



Classic, Table-desktop, Hybrid
```
"settings": {
	{
		vmlBackground: true,
		rolePresentation: false,
		encodeUrls: true,
		lineLength: 799,
		lang: "en",
		buttonType: "classic",
		templatingLanguage: "handlebars",
		generatorMode: "table-desktop",
	}
}
```