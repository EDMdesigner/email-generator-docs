# Body element (Root element)

Every document starts with this element, as this is the top parent element. In the old JSON format of our editors (EDMdesigner, Chamaileon) it is equal to the `root` element. It contains a children array with a full width container as a child. In the old JSON format of our editors it has no other property out of the children field, but the new generator accept a more logical structure beside the old format too. 
The main difference is the background property, that defines the background of the HTML `<body>` tag, is the first property of the body. This property is placed in the generalSettings in the old JSON format.

The old format (the generator will convert it, no manual changing is needed):
```
"document" : {
	"root" : {
		"children" : [ 
			...
		],
		"type" : "ROOT"
	}
	"generalSettings" : {
		"background" : {
			"image" : {
				"src" : "https://example.png",
				"repeat" : "no-repeat",
				"position" : "center center"
			},
			"color" : "#60de55"
		}
	}
}
```


The new format: 
```
"document" : {
	"body" : {
		"background" : {
			"color" : "#60de55",
			"image" : {
				"src" : "https://example.png",
				"repeat" : "both",
				"position" : "center"
			}
		},
		"children": [
			...
		]
	},
	"head" : {
		...
	},
	"settings" : {
		...
	}
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
body | object | object | this wrapper property contains all the elements of the email content
body.background| object | object | set a background around the email content container, it is visible, if the view pane is wider than the widest fullwith container. [More about background properties](/property-groups/background/README.md)
children | array | | The children array may [contain any of our element types](/elements)
settings | object | object | set the generator's general settings, like accessibility settings and line breaks


