##GE Power Data Time Series Data for Hackathon

This document provides details on the data that can be used for Minds and Machines Hackathon November 2016 in San Francisco. This document is not intended to provide details of the hackathon challenge and assumes that the users are provided with the details of the challenge.

A predix time series instance is set up and contains the data that can be used during the hackathon to build applications. For more information about time series, follow the documentation on predix.io (https://www.predix.io/docs#mnlfuvZz). This data available for hackathon is readonly.

##Cloud Foundry Enviroment
The timeseries users have access to the following cloud foundry org and space.
  * _org_: predix_builders
  * _space_: hackhub 
  
##Accessing Time Series Data
Time series data can be accessed programatically using Time Series Client Library and the documentation is provided under https://www.predix.io/docs#IGxiMSFj. To access the time series instance, we need the following information.

* UAA to perform authentication and to get authentication token
* Time Series Instance details to access time series using the obtained authentication token.

The following UAA and Time Series details are needed for the data retrieval.

* **UAA URL**: https://98d4176d-a268-405b-a461-3f9944793a31.predix-uaa.run.aws-usw02-pr.ice.predix.io/oauth/token
* **Client Name**: app_client_id
* **Client Password**: secret
* **TimeSeries Query URL**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/
  * **Query tags**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/tags
  * **Query datapoints**: https://time-series-store-predix.run.aws-usw02-pr.ice.predix.io/v1/datapoints
* **Timeseries Predix-Zone-Id**: e3fba85e-d334-409e-87ce-3a17e71b4946




 




