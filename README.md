# Email generator documentation

## Making requests

Our API is super simple. You have to make a HTTP POST request with a `Content-Type: application/json` header to the following url from your backend:

```
https://api.emailml.com/v1/<YOUR_API_KEY>/email-html
```

The body of the request should look like this:

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": { ... }
}
```

DOCUMENT FORMAT DESCRIPTION COMES LATER. Until then, we are providing some example JSONs in the jsons folder in this repository. You only need the "document" property from those JSONS and you have to put it to the "document" property of the HTTP POST request. The other way is that you put your apiKey and secret in the JSON's root and you send them together.

The response is a JSON with the following format:

```
{
	"status": 200,
	"result": "The response HTML as a string."
}
```

---

For EDMdesigner integrators: You can use the JSON documents fetched from EDMdesigner's API. Similarly, you will only need the "document" property from those JSONs. We are going to direct the traffic from the original generator route to this one in the future. At the moment, this service is for testing purposes only!

## Generator settings

With the settings object you can change the behaviour of the generator. You find every option's description in the [document-settings folder](https://github.com/EDMdesigner/email-generator-docs/tree/master/document-settings) :

```
{
	"apiKey": "<YOUR_API_KEY>",
	"secret": "<YOUR_API_SECRET>",
	"document: { ... },
	"settings": {
		vmlBackground: true,
		rolePresentation: false,
		lineLength: 799,
		encodeUrls: true,
		"lang": "fr"
	}
}
```

## Release Toggles

Whenever we release new features we do it behind a release toggle. It means that if you don't explicitly turn on that feature, then our email HTML generator's output will be unchanged.
This way we can make it sure that nothing breaks on your backend.

For example, you might need to add tracking code to our buttons. You can do it by searching for a certain class name in our output and replace the link there.
But what happens if our output changes? Well, without feature toggles, adding the tracking code might break on your backend, since you won't find that class name in our output.

By releasing new features behind feature toggles, it's not a problem at all. You can explicitly turn on the new feature in your test environment and modify your backend in order to work with the new feature.

If you want to learn more about feature toggles, please read [Martin Fowler's article](https://martinfowler.com/articles/feature-toggles.html).

## The release process

1. We are going to notify you about all of the changes in the generator
	- You will have access to the description of every feature/fix (while they are behind a feature toggle), and you will be able to check out how that feature changes the email HTML code
	- You are going to receive an email when a new feature/fix is available behind a feature flag
2. When a new feature is ready, we release it behind a feature toggle.
	- You will be able to turn the new features on and off, this way you will be able to experiment with the new features and fixes
	- You will be able to give us feedback
	- You will be able to change your backend code if needed before pushing it into production
	- You will have the opportunity to decide when you want to turn the feature on in production
	- And finally, if something goes wrong, you can turn off the feature any time by flipping a boolean value
3. Every new feature and fix will stay behind a feature toggle for a month
	- It will give everyone using our service enough time to prepare their backend for the new feature/changes
	- If it comes out that there is a better solution for something, we can drop a feature after that month
4. We are going to infrom you if something behind a feature toggle will become the default behaviour
	- You are going to receive an email beforehand (at least a week) if a feature will turn into the default behavior
	- And you are going to receive an email beforehand (at least a week) when a feature behind a feature flag will be dropped
	
## Compatibility

We are proud that our HTML generator supports the major email clients and also a lot less popular ones. We frequently test the output to maintain quality. For the full list of our supported email clients please check [our page about compatibility](https://github.com/EDMdesigner/email-generator-docs/tree/master/compatibility) and if you don't find the email client you looking for or you experience some issue please do not hesitate to create an issue in [our issue tracking repository] (https://github.com/EDMdesigner/editor-issues/issues).
