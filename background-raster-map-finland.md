**Under Construction!!!!**

The below example Open Data Product Specification is created by ODPS developers and is not official version. You can find the original information of National Land Survey of Finland´s Background map (raster) from https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/expert-users/product-descriptions/background-map-series-raster

This example is the compact version data product description you can you with ODPS. Also the open data license link is added with extension function instead of using ODPS built-in machine-readable formatting.

Example with Open Data Product Specification 2.1. https://open-data-product-initiative.github.io/open-data-product-spec-2.1

```
{
   "product":{
      "en":{
         "name":"NLS Background map (raster)",
         "productID":"nls001",
         "valueProposition":"The Background map is a dataset product series in raster format that depicts the whole of Finland and that is meant for web use as a background material for thematic data. Its key objects are road names, roads and railways, buildings and constructions, administrative borders, geographical names, waterways, land use and addresses of buildings (from the Digital and             Population Data Services Agency). The product belongs to the open data of the National Land Survey of Finland.",         
         "visibility":"public",
         "status":"production",
         "version":"1.0",
         "x-license": "https://data.gov.sg/open-data-licence",
         "categories":[
            "environment, open data, government, geospatial"
         ],
         
         "tags":[
            "maps, geospatial, NLS, National Land Survey of Finland" 
         ],
         "brandSlogan":"Information about the Earth.",
         "type":"dataset",
         "logoURL":"https://www.maanmittauslaitos.fi/themes/custom/mml/images/english_logo_rgb.svg",
         "OutputFileFormats":[
            "png",
            "jpg"
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

      "dataAccess":{
         "type":"API",
         "authenticationMethod":"None",
         "specification":"OAS",
         "format":"JSON",
         "documentationURL":"https://data.gov.sg/dataset/ultraviolet-index-uvi"
      
     
      },
      "dataHolder":{
       
         "businessDomain":"National Land Survey of Finland",
         "logoURL":"https://www.maanmittauslaitos.fi/themes/custom/mml/images/english_logo_rgb.svg",
         "description":"The National Environment Agency (NEA) is the leading public organisation responsible for ensuring a clean and sustainable environment for Singapore. Its key roles are to improve and sustain a clean environment, promote sustainability and resource efficiency, maintain high public health standards, provide timely and reliable meteorological information, and encourage a vibrant hawker culture. NEA works closely with its partners and the community to develop and spearhead environmental and public health initiatives and programmes. It is committed to motivating every individual to care for the environment as a way of life, in order to build a liveable and sustainable Singapore for present and future generations.",
         "URL":"https://www.nls.fi/",
         "addressCountry":"Finland",
         "slogan":"A clean environment, towards a liveable and sustainable Singapore."
      }
   }
}
