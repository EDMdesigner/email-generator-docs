# Set up UTM parameters for every link

## About UTM parameters

By adding campaign parameters to the destination URLs you use in your ad campaigns, you can collect information about the overall efficacy of those campaigns, and also understand where the campaigns are more effective. [Source](https://support.google.com/analytics/answer/1033863?visit_id=637571114704260347-3467735685&rd=1#zippy=%2Cin-this-article)

## Implementation

The generator appends every `key` & `value` parameter to every link that has the `https://` protocol.


Example JSON:

```
	"document": {
		"body": {
			...
		},
		"head": {
			...
		},
		"utm": {
			"generate": true,
			"parameters": [
				{
					"key": "utm_source",
					"value": "value1"
				},
				{
					"key": "utm_medium",
					"value": "value2"
				},
				{
					"key": "utm_campaign",
					"value": "value3"
				},
				{
					"key": "utm_term",
					"value": "value4"
				},
				{
					"key": "utm_content",
					"value": "value5"
				},
				{
					"key": "key1",
					"value": "value6"
				}
			]
	},
	}
```

Properties | Type | Values | Description
--- | --- | --- | ---
UTM | object | object | this wrapper property contains all the UTM elements
UTM.generate | | boolean | if it's set to true, the generator will add the parameters to every `https://` link
UTM.parameters| array | array | this wrapper property contains the UTM parameters
UTM.parameters[object] | object | object | this wrapper contains one key and it's value. They are freely customizable and there are no required keys.
UTM.parameters[object].key | string | short text | this is the name of the UTM parameter. Example: `utm_campaign`
UTM.parameters[object].value | string | short text | this is the value of the UTM parameter. Example: `summer_sale`