
# Ultra-violet Index (UVI) MVP with license url extension

The below example Open Data Product Specification is created by ODPS developers and is not official version. You can find the original information of the Ultra-violet Index (UVI) from https://data.gov.sg/dataset/ultraviolet-index-uvi 

This example is the compact version data product description you can you with ODPS. Also the open data license link is added with extension function instead of using ODPS built-in machine-readable formatting. 

Example with Open Data Product Specification 2.1. https://open-data-product-initiative.github.io/open-data-product-spec-2.1 

```
{
	"product": {
		"en": {
			"name": "Hourly Singapore Ultra-violet values data API",
			"productID": "sg01",
			"valueProposition": "UV Index value averaged over the past hour. Updated every hour between 7 AM and 7 PM everyday.",
			"description": "National Environment Agency provides APIs for readings of temperature, humidity, precipitation and wind conditions at up to one-minute intervals. The data is provided at weather-station level.",
			"visibility": "public",
			"status": "production",
			"version": "1.0",
			"x-license": "https://data.gov.sg/open-data-licence",
			"categories": [
				"environment, open data, government"
			],
			"tags": [
				"ultra-violet, hourly, daily, API, National Environment Agency"
			],
			"brandSlogan": "A clean environment, towards a liveable and sustainable Singapore.",
			"type": "dataset",
			"logoURL": "https://data-product-business.github.io/open-data-product-spec/images/logo-dps-ebd5a97d.png",
			"OutputFileFormats": [
				"json"
			]
		},
		"recommendedDataProducts": [
			"https://data.gov.sg/dataset/weather-forecast",
			"https: //data.gov.sg/dataset/realtime-weather-readings",
			"https://data.gov.sg/dataset/pm2-5"
		],
		"pricingPlans": {
			"en": [{
					"name": "Freemium Open Data API",
					"priceCurrency": "EUR",
					"price": "0.00",
					"billingDuration": "year",
					"unit": "open-data",
					"maxTransactionQuantity": "unlimited"
				}
			]
		},
		"dataAccess": {
			"type": "API",
			"authenticationMethod": "None",
			"specification": "OAS",
			"format": "JSON",
			"documentationURL": "https://data.gov.sg/dataset/ultraviolet-index-uvi"
		},
		"dataHolder": {

			"businessDomain": "National Environment Agency",
			"logoURL": "https://www.nea.gov.sg/assets/images/design/logo.png",
			"description": "The National Environment Agency (NEA) is the leading public organisation responsible for ensuring a clean and sustainable environment for Singapore. Its key roles are to improve and sustain a clean environment, promote sustainability and resource efficiency, maintain high public health standards, provide timely and reliable meteorological information, and encourage a vibrant hawker culture. NEA works closely with its partners and the community to develop and spearhead environmental and public health initiatives and programmes. It is committed to motivating every individual to care for the environment as a way of life, in order to build a liveable and sustainable Singapore for present and future generations.",
			"URL": "https://www.nea.gov.sg/",
			"addressCountry": "Singapore",
			"slogan": "A clean environment, towards a liveable and sustainable Singapore."
		}
	}
}
```
