##GE Power Data Time Series Data for Hackathon
This document provides details on the data that can be used for Minds and Machines Hackathon November 2016 in San Francisco. This document is not intended to provide details of the hackathon challenge and assumes that the users are provided with the details of the challenge.

The Waukesha Engine is a product of GE Power that is natural gas based. It is used to power a variety of different applications ranging from powering isolated communities to usage within natural gas production applications.
More comprehensive information regarding the Waukesha Engine can be found here. [More Information](https://powergen.gepower.com/content/dam/gepower-pgdp/global/en_US/documents/product/Reciprocating%20Engines/waukesha-powering-the-world-brochure.pdf)
A predix time series instance is set up and contains the data that can be used during the hackathon to build applications. For more information about time series, follow the documentation on predix.io (https://www.predix.io/docs#mnlfuvZz). This data available for hackathon is readonly.

##Cloud Foundry Enviroment
The timeseries users have access to the following cloud foundry org and space.
  * _org_: predix_builders
  * _space_: hackhub 
  
##Environment Details for Accessing Time Series Data
Time series data can be accessed programatically using Time Series Client Library and the documentation is provided under https://www.predix.io/docs#IGxiMSFj. To access the time series instance, we need the following information.

* UAA to perform authentication and to get authentication token
* Time Series Instance details to access time series using the obtained authentication token.

The following UAA and Time Series details are needed for the data retrieval.

* **UAA URL**: https://98d4176d-a268-405b-a461-3f9944793a31.predix-uaa.run.aws-usw02-pr.ice.predix.io/oauth/token
* **Client Name**: _To be handed out during the hackathon_
* **Client Password**: _To be handed out during the hackathon_
* **TimeSeries Query URL**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/
  * **Query tags**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/tags
  * **Query datapoints**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/datapoints
* **Timeseries Predix-Zone-Id**: e3fba85e-d334-409e-87ce-3a17e71b4946

The time series connection can be verified quickly using the predix starter kit (https://predix-toolkit.run.aws-usw02-pr.ice.predix.io), prior to using the predix client libraries in the code. 

##Time Series Query
The following is a sample query to retieve the data using one of the tags 


{  
  
  "start":"1d-ago",
  
   "tags":[ 
   
      {  
      
         "name":"Engine Oil Pressure",
         
         "order":"desc",
         
         "filters":{  
         
            "attributes":{  
            
               "AssetUri":"/engine/2afbd553-8d7f-4c59-8346-d93a92b177ba"
               
            }
            
         }
         
      }
      
   ]
   
}


The following are the available tags in time series for the query:
* Engine Frequency
* Engine Hours
* Engine LB Exhaust Temp
* Engine Load
* Engine Oil Pressure
* Engine Oil Temp
* Engine Power
* Engine Power - Insights
* Engine RB Exhaust Temp
* Engine Speed

The following are the available Asset URIs for the query:
* /engine/2afbd553-8d7f-4c59-8346-d93a92b177ba
* /engine/cb27ef1b-b0de-494d-877f-32e95b757651
* /engine/86d23000-3820-4d56-b755-6ea1302ddc4b
* /engine/892e596d-3sds-4c9e-9094-078245931785
* /engine/049bb0c2-fca8-4fc6-af28-558c57a1de86
* /engine/14727426-d32e-4feb-a2ec-a89f8c5ab100
* /engine/28880fbe-cb5a-40a7-a885-de4683528fbe
* /engine/2afbd546-8d7f-4c59-8346-d93a92b177ba
* /engine/6f3cd880-2ad8-43ae-a194-08e2400be4bd
* /engine/86d23000-3820-1234-b755-6ea1302ddc4b
* /engine/892e596d-e734-4c9e-9094-078245931785
* /engine/8c12e00a-7d73-42a5-aef3-8f87298d6748
* /engine/99fefd4b-6503-4e9f-81e4-4a35acd336a8
* /engine/af1135b8-e3a7-4938-967d-4783a8ebafe5
* /engine/cd37ef1b-b0de-494d-877f-32e95b757651
 




