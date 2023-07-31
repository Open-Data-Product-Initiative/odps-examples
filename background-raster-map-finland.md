# National Land Survey of Finland: Background Maps (raster)

The below example Open Data Product Specification is created by ODPS developers and is not official version. You can find the original information of National Land Survey of Finland´s Background map (raster) from https://www.maanmittauslaitos.fi/en/maps-and-spatial-data/expert-users/product-descriptions/background-map-series-raster

This example is the compact version data product description you can you with ODPS. Also the open data license link is added with extension function instead of using ODPS built-in machine-readable formatting.

Example with Open Data Product Specification 2.1. https://open-data-product-initiative.github.io/open-data-product-spec-2.1

```
{
   "product":{
      "en":{
         "name":"NLS Background map (raster)",
         "productID":"nls001",
         "valueProposition":"The Background map is a dataset product series in raster format that depicts the whole of Finland and that is meant          for web use as a background material for thematic data. Its key objects are road names, roads and railways, buildings and                        constructions, administrative borders, geographical names, waterways, land use and addresses of buildings (from the Digital and                  Population Data Services Agency). The product belongs to the open data of the National Land Survey of Finland.",
         "description": "The data content of the Background map series according to background map rasters:
         The data content becomes larger as the scale increases. The data content includes objects that are essential when locating your                  position. The images have been anti-aliased.",
         "visibility":"public",
         "status":"production",
         "x-license": "https://creativecommons.org/licenses/by/4.0/",
         "x-geographicLocation": "Entire Finland",
         "x-spatialRepresentation": "Raster",
         "x-coordinateReferenceSystem": [
         "EPSG:3067"
         ],
         "x-scales":[
            "1:5000",
            "1:10000",
            "1:20000",
            "1:40000",
            "1:80000",
            "1:160000",
            "1:320000",
            "1:800000",
            "1:2000000",
            "1:4000000",
            "1:8000000"
            ],
         "x-pixelSizeMeters":[
            "0.5",
            "2",
            "4",
            "8"
            "16",
            "32",
            "64",
            "128",
            "256"
            "1024",
            "2048"
            ],
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
            "png"
         ]
         
      },
      "recommendedDataProducts":[
          "https://www.maanmittauslaitos.fi/maastotietokannan-kyselypalvelu" 
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
         "type":"WMTS",
         "authenticationMethod":"API Key",
         "documentationURL":"https://www.maanmittauslaitos.fi/karttakuvapalvelu/tekninen-kuvaus-wmts"     
      },
      "dataHolder":{      
         "businessDomain":"National Land Survey of Finland",
         "logoURL":"https://www.maanmittauslaitos.fi/themes/custom/mml/images/english_logo_rgb.svg",
         "description":"The National Land Survey of Finland safeguards the land ownership and credit system by maintaining information about properties and housing company shares in its registers and takes care of the registration of ownership and mortgages. Other tasks of the agency include spatial data research and application.",
         "URL":"https://www.nls.fi/",
         "addressCountry":"Finland",
      }
   }
}
