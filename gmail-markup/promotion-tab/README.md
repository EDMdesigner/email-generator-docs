# Set a Promotion Card

## What is a Promotion Card?

Gmail came up with an update that, by using machine learning, it automatically groups and highlights emails in the Promotions tab that people are most likely to engage with.
Gmail identifies the most valuable messages for each user and groups them into bundles organized by topic or themes like Top Deals or Top Picks.

The new features include Single Image Previews, Deal Badges and Custom Logos. These components can be combined to a Promotion Card.

Google terms these features as Annotations as senders would “annotate” the emails with Schema markup that allows Gmail to pick up these features.

More about the Promotion Card:
 - https://developers.google.com/gmail/promotab/overview
 - https://developers.google.com/gmail/promotab/best-practices

## Implementation

Gmail allows two options to embed Schema data. The JSON-LD snippet usually goes in the head of the email, the Microdata fits better in the email body. Read more about the formats [here](https://developers.google.com/gmail/markup/reference/formats/json-ld) and here [here](https://developers.google.com/gmail/markup/reference/formats/microdata).
Some Email Service Providers strip the JSON-LD code as it is embedded within a script tag, be aware of your ESP's policy.

The generator puts the data defined by you in both formats, the JSON-LD is placed in the head, the microdata part is in the body tag.


Example JSON:

```json
{
	"document": {
		"body": {
			...
		},
		"head": {
			...
		},
		"gmail": {
			"promotion": {
				"generate": true,
				"logo": "https://images.examples.png",
				"description": "20% OFF",
				"discountCode": "PROMO-25%OFF",
				"availabilityStarts": "2020-07-16T17:06:18+02:00",
				"availabilityEnds": "2020-07-23T00:00:00",
				"image": "https://images.examples2.png"
			}
		}
	}
}
```

Properties | Type | Values | Description
--- | --- | --- | ---
gmail | object | object | this wrapper property contains all the gmail markup elements
gmail.promotion| object | object | this wrapper property contains the properties of the gmail promotion tab
gmail.promotion.generate | | boolean | if it's set to true, the generator will generate JSON-LD and microdata code snippets in the email HTML
gmail.promotion.logo | string | url | the url of the logo image. Be sure to use an https url
gmail.promotion.description | string | short text | Highlight any offerings. Avoid using more than four words or full sentences in this space, as it competes with your subject line.
gmail.promotion.discountCode | string | short text | use a discount code if you have it featured in the email
gmail.promotion.availabilityStarts | string | the start date of the discount |[Read more on the date format](https://support.google.com/merchants/answer/7055760)
gmail.promotion.availabilityEnds | string | the end date of the discount |[Read more on the date format](https://support.google.com/merchants/answer/7055760)
gmail.promotion.image | string | url | the url of an image you want to use to highlight in the promotion tab. Be sure to use an https url and the dimensions of the image are 538 x 138 pixels in size and have a 3.9 aspect ratio
