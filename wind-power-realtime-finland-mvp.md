
# Wind power production - real time data with x-license extensions

The below example Open Data Product Specification is created by ODPS developers and is not official version. You can find the original information of the Wind power production - real time data from https://data.fingrid.fi/en/dataset/wind-power-production-real-time-data 

This example is the compact version data product description you can you with ODPS. Also the open data license link is added with extension function instead of using ODPS built-in machine-readable formatting. 

Example with Open Data Product Specification 2.1. https://open-data-product-initiative.github.io/open-data-product-spec-2.1 

```
{
	"product": {
		"en": {
			"name": "Wind power production - real time data",
			"productID": "fi01",
			"description": "Wind power production based on the real-time measurements in Fingrid's operation control system. About two percent of the production capacity is estimated as measurements aren't available. The data is updated every 3 minutes.",
			"visibility": "public",
			"status": "production",
			"x-license": "http://www.opendefinition.org/licenses/cc-by",
			"version": "1.0",
			"categories": [
				"energy, open data, government"
			],

			"tags": [
				"Real time data, Wind power"
			],
			"brandSlogan": "Open data on the electricity market and the power system",
			"type": "dataset",
			"logoURL": "https://data-product-business.github.io/open-data-product-spec/images/logo-dps-ebd5a97d.png",
			"OutputFileFormats": [
				"json",
				"xml",
				"csv"
			]
		},
		"fi": {
			"name": "Tuulivoimatuotanto - reaaliaikatieto ",
			"productID": "fi01",
			"description": "Tuulivoiman hetkellinen tuotantoteho Fingridin käytönvalvontajärjestelmän mittaustiedoista. Noin kaksi prosenttia tuotantokapasiteetista on arvioitua, sillä mittaustietoa ei ole saatavilla. Tieto päivitetään 3 minuutin välein.",
			"visibility": "public",
			"status": "production",
			"x-license": "http://www.opendefinition.org/licenses/cc-by",
			"version": "1.0",
			"categories": [
				"energy, open data, government"
			],

			"tags": [
				"Tuulivoima, Reaaliaikatieto"
			],
			"brandSlogan": "Avointa dataa sähkömarkkinoista ja voimajärjestelmästä",
			"type": "dataset",
			"logoURL": "https://data-product-business.github.io/open-data-product-spec/images/logo-dps-ebd5a97d.png",
			"OutputFileFormats": [
				"json",
				"xml",
				"csv"
			]
		},
		"dataAccess": {
			"type": "API",
			"authenticationMethod": "API Key",
			"specification": "OAS",
			"format": "HTML",
			"documentationURL": "https://data.fingrid.fi/en/dataset/wind-power-production-real-time-data"
		},

		"pricingPlans": {
			"en": [{
				"name": "Freemium Open Data API",
				"priceCurrency": "EUR",
				"price": "0.00",
				"billingDuration": "year",
				"unit": "open-data",
				"maxTransactionQuantity": "unlimited"
			}],
			"fi": [{
				"name": "Ilmainen avoindata API",
				"priceCurrency": "EUR",
				"price": "0.00",
				"billingDuration": "year",
				"unit": "open-data",
				"maxTransactionQuantity": "unlimited"
			}]
		},

		"dataAccess": {
			"type": "API",
			"authenticationMethod": "None",
			"specification": "OAS",
			"format": "JSON",
			"documentationURL": "https://data.gov.sg/dataset/ultraviolet-index-uvi"
		},
		"SLA": {
			"updateFrequency": {
				"unit": "hours",
				"value": 3
			},
			"uptime": {
				"unit": "string",
				"value": "best effort"
			},
			"support": {
				"company": {
					"email": "aino.summanen@fingrid.fi",
					"guidesURL": "https://data.fingrid.fi/en/pages/faq"
				}
			}
		},
		"dataHolder": {
			"businessDomain": "Fingrid",
			"logoURL": "https://data.fingrid.fi/logo_en.png",
			"description": "Fingrid Oyj is the enterprise which takes care of the functioning of the nation-wide high-voltage grid, the backbone of electricity transmission. We transmit electricity continuously from electricity generating companies to distribution network companies and industrial companies. We take care of the cross-border connections and promote the functioning of the electricity market. ",
			"URL": "https://data.fingrid.fi/en/",
			"addressCountry": "Finland",
			"slogan": "Open data on the electricity market and the power system"
		}
	}
}
```
