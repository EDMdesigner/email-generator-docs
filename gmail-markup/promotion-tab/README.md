```
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
```

Properties | Type | Values | Description
--- | --- | --- | ---
gmail | object | object | this wrapper property contains all the gmail markup elements
gmail.promotion| object | object | this wrapper property contains the properties of gmail promotion tab
gmail.promotion.generate | | boolean | 
gmail.promotion.logo | string | url | the url of the logo image. Be sure to use an https url
gmail.promotion.description | string | short text | Highlight any offerings. Avoid using more than four words or full sentences in this space, as it competes with your subject line.
gmail.promotion.discountCode | string | short text | use a discount code if you have it featured in the email
gmail.promotion.availabilityStarts | string | the start date of the discount |[Read more on the date format](https://support.google.com/merchants/answer/7055760)
gmail.promotion.availabilityEnds | string | the end date of the discount |[Read more on the date format](https://support.google.com/merchants/answer/7055760)
gmail.promotion.image | string | url | the url of an image you want to use to highlight in the promotion tab. Be sure to use an https url and the dimensions of the image are 538 x 138 pixels in size and have a 3.9 aspect ratio