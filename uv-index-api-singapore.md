
# Ultra-violet Index (UVI)

The below example Open Data Product Specification is created by ODPS developers and is not official version. You can find the original information of the Ultra-violet Index (UVI) from https://data.gov.sg/dataset/ultraviolet-index-uvi 

Example with Open Data Product Specification 2.1. https://open-data-product-initiative.github.io/open-data-product-spec-2.1 

```
{
   "product":{
      "en":{
         "name":"Hourly Singapore Ultra-violet values data API",
         "productID":"sg01",
         "valueProposition":"UV Index value averaged over the past hour. Updated every hour between 7 AM and 7 PM everyday.",
         "description":"National Environment Agency provides APIs for readings of temperature, humidity, precipitation and wind conditions at up to one-minute intervals. The data is provided at weather-station level.",
         "productSeries":"",
         "visibility":"public",
         "status":"production",
         "version":"1.0",
         "categories":[
            "environment, open data, government"
         ],
         "standards":[
            ""
         ],
         "tags":[
            "ultra-violet, hourly, daily, API, National Environment Agency" 
         ],
         "brandSlogan":"A clean environment, towards a liveable and sustainable Singapore.",
         "type":"open data",
         "logoURL":"https://data-product-business.github.io/open-data-product-spec/images/logo-dps-ebd5a97d.png",
         "OutputFileFormats":[
            "json"
         ],
         "useCases":[
            
         ]
      },
      "recommendedDataProducts":[
          "https://data.gov.sg/dataset/weather-forecast, 
          https://data.gov.sg/dataset/realtime-weather-readings",
          "https://data.gov.sg/dataset/pm2-5"
          ],      
      "pricingPlans":{
         "en":[
            {
               "name":"Freemium Open Data API",
               "priceCurrency":"EUR",
               "price":"0.00",
               "billingDuration":"year",
               "unit":"open-data",
               "maxTransactionQuantity":"unlimited"
            },
            
         ]
      },
      "dataOps":{
        
      },
      "dataAccess":{
         "type":"API",
         "authenticationMethod":"None",
         "specification":"OAS",
         "format":"JSON",
         "documentationURL":"https://data.gov.sg/dataset/ultraviolet-index-uvi"
      },
      "dataQuality":{
         "accuracy":100,
         "completeness":100,
         "consistency":100,
         "timeliness":"high",
         "validity":100,
         "uniqueness":100,
         "dataQualityAssuranceMethods":"Data quality assurance suite of tools and methods include both data quality auditing (DQA) tools designed for use by external audit teams and routine data quality assessment (RDQA) tools designed for capacity building and self-assessment."
      },
      "SLA":{
         "updateFrequency":{
            "unit":"hours",
            "value":1
         },
         "uptime":{
            "unit":"percentage",
            "value":99
         },
         "responseTime":{
            "unit":"milliseconds",
            "value":200
         },
         "nullValues":{
            "unit":"percentage",
            "value":0.01
         },
         "support":{
            "company":{
               "phoneNumber":"",
               "phoneServiceHours":"",
               "chatURL":"",
               "chatServiceHours":"",
               "chatResponseTime":"",
               "email":"",
               "emailServiceHours":"",
               "emailResponseTime":"",
               "documentationURL":"",
               "guidesURL":""
            },
            "community":{
              
            }
         },
         "observability":{
            
         }
      },
      "license":{
         "scope":{
            "definition":"The purpose of this license is to determine the terms and conditions applicable to the licensing of the data product, whereby Data Holder grants Data User the right to use the data.",
            "language":"en-us",
            "restrictions":"Data User agrees not to, directly or indirectly, participate in the unauthorized use, disclosure or conversion of any confidential information.",
            "geographicalArea":[
               "EU",
               "US"
            ],
            "permanent":false,
            "exclusive":false,
            "rights":[
               "Display",
               "Distribution",
               "Adaptation",
            ]
         },
         "privacy":{
            "containsPersonalData":false,
            "applicaplePrivacyLaws":[
               
            ],
         },
         "termination":{
            "terminationConditions":"Cancellation before 30 days. After the expiry of the right of use, the product and its derivatives must be removed.",
            "continuityConditions":"Expired license will automatically continued without written cancellation (termination) by Data Holder"
         },
         "governance":{
            "damages":"During the term of license, except for the force majeure or the Data Holders reasons, Data User is required to follow strictly in accordance with the license. If Data User wants to terminate the license early, it needs to pay a certain amount of liquidated damages.",
            "confidentiality":"Data User undertakes to maintain confidentiality as regards all information of a technical (such as, by way of a non-limiting example, drawings, tables, documentation, formulas and correspondence) and commercial nature (including contractual conditions, prices, payment conditions) gained during the performance of this license.",
            "applicableLaws":"This license shall be interpreted, construed and enforced in accordance with the law of Finland, Incl. Copyright Act 404/1961.",
            "warranties":"Data Holder makes no warranties, express or implied, guarantees or conditions with respect to your use of the data product. To the extent permitted under local law, Data Holder disclaims all liability for any damages or losses, including direct, consequential, special, indirect, incidental or punitive, resulting from Data User use of the data product.",
            "audit":"Data Holder will reasonably cooperate with Data User by providing available additional information concerning the data product. Each party will bear its own costs with respect to the audit procedures.",
            "forceMajeure":"Each party may suspend the fulfilment of its contractual obligations, when the said fulfilment is impossible or objectively too costly due to an unforeseeable impediment independent from the parties, such as for example: strike, boycott, lockout, fire, war (declared or not), civil war, riots and revolutions, requisitions, embargo, power blackouts, extraordinary breakage of machinery, delays in the delivery of components or raw materials."
         }
      },
      "dataHolder":{
         "taxID":"",
         "vatID":"",
         "businessDomain":"National Environment Agency",
         "logoURL":"https://www.nea.gov.sg/assets/images/design/logo.pngg",
         "description":"The National Environment Agency (NEA) is the leading public organisation responsible for ensuring a clean and sustainable environment for Singapore. Its key roles are to improve and sustain a clean environment, promote sustainability and resource efficiency, maintain high public health standards, provide timely and reliable meteorological information, and encourage a vibrant hawker culture. NEA works closely with its partners and the community to develop and spearhead environmental and public health initiatives and programmes. It is committed to motivating every individual to care for the environment as a way of life, in order to build a liveable and sustainable Singapore for present and future generations.",
         "URL":"https://www.nea.gov.sg/",
         "addressRegion":" Singapore",
         "addressLocality":"Singapore",
         "addressCountry":"Singapore",
         "aggregateRating":"",
         "ratingCount":,
         "slogan":"A clean environment, towards a liveable and sustainable Singapore.",
         "parentOrganization":""
      }
   }
}
```