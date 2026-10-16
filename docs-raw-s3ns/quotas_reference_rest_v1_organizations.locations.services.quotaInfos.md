# REST Resource: organizations.locations.services.quotaInfos

Source: https://documentation.s3ns.fr/docs/quotas/reference/rest/v1/organizations.locations.services.quotaInfos
Last updated: 2026-01-21

Some or all of the information on this page might not apply to Cloud de Confiance by S3NS. See [Differences from Google Cloud](/docs/quotas/tpc-differences) for more details.














- 





[

Home

](https://documentation.s3ns.fr/)






- 








[

Documentation

](https://documentation.s3ns.fr/docs)






- 








[

Cloud Quotas

](https://documentation.s3ns.fr/docs/quotas)






- 








[

Reference

](https://documentation.s3ns.fr/docs/quotas/apis)












# REST Resource: organizations. locations. services. quota Infos 






- On this page 
- [ Resource: QuotaInfo ](#resource:-quotainfo)
- [ Methods ](#methods)

- [ get ](#get)
- [ list ](#list)

- 















- [Resource: QuotaInfo](#QuotaInfo)



- [JSON representation](#QuotaInfo.SCHEMA_REPRESENTATION)





- [Methods](#METHODS_SUMMARY)





## Resource: Quota Info 




QuotaInfo represents information about a particular quota for a given project, folder or organization.






| 
JSON representation | 
|



| 

```
{ 
"name" : string , 
"quotaId" : string , 
"metric" : string , 
"service" : string , 
"isPrecise" : boolean , 
"refreshInterval" : string , 
"containerType" : enum (`[ContainerType](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.ContainerType)`) , 
"dimensions" : [ 
string 
] , 
"metricDisplayName" : string , 
"quotaDisplayName" : string , 
"metricUnit" : string , 
"quotaIncreaseEligibility" : { 
object (`[QuotaIncreaseEligibility](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.QuotaIncreaseEligibility)`) 
} , 
"isFixed" : boolean , 
"dimensionsInfos" : [ 
{ 
object (`[DimensionsInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.DimensionsInfo)`) 
} 
] , 
"isConcurrent" : boolean , 
"serviceRequestQuotaUri" : string 
} 
```
| 
|











| 
Fields | 
|



| 
`name` | 



`string`



Resource name of this QuotaInfo. The ID component following "locations/" must be "global". For example, `projects/123/locations/global/services/compute.googleapis.com/quotaInfos/CpusPerProjectPerRegion`

| 
|

| 
`quota Id` | 



`string`



The id of the quota, which is unique within the service. For example, `CpusPerProjectPerRegion`

| 
|

| 
`metric` | 



`string`



The metric of the quota. It specifies the resources consumption the quota is defined for. For example, `compute.googleapis.com/cpus`

| 
|

| 
`service` | 



`string`



The name of the service in which the quota is defined. For example, `compute.googleapis.com`

| 
|

| 
`isPrecise` | 



`boolean`



Whether this is a precise quota. A precise quota is tracked with absolute precision. In contrast, an imprecise quota is not tracked with precision.

| 
|

| 
`refreshInterval` | 



`string`



The reset time interval for the quota. Refresh interval applies to rate quota only. For example, "minute" for per minute, "day" for per day, or "10 seconds" for every 10 seconds.

| 
|

| 
`containerType` | 



`enum ( [ContainerType](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.ContainerType)`) 



The container type of the QuotaInfo.

| 
|

| 
`dimensions[]` | 



`string`



The dimensions the quota is defined on.

| 
|

| 
`metricDisplayName` | 



`string`



The display name of the quota metric

| 
|

| 
`quotaDisplayName` | 



`string`



The display name of the quota.

| 
|

| 
`metricUnit` | 



`string`



The unit in which the metric value is reported, e.g., "MByte".

| 
|

| 
`quotaIncreaseEligibility` | 



`object ( [QuotaIncreaseEligibility](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.QuotaIncreaseEligibility)`) 



Whether it is eligible to request a higher quota value for this quota.

| 
|

| 
`isFixed` | 



`boolean`



Whether the quota value is fixed or adjustable

| 
|

| 
`dimensionsInfos[]` | 



`object ( [DimensionsInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.DimensionsInfo)`) 



The collection of dimensions info ordered by their dimensions from more specific ones to less specific ones.

| 
|

| 
`isConcurrent` | 



`boolean`



Whether the quota is a concurrent quota. Concurrent quotas are enforced on the total number of concurrent operations in flight at any given time.

| 
|

| 
`serviceRequestQuotaUri` | 



`string`



URI to the page where users can request more quota for the cloud service—for example, [https://console.cloud.google.com/iam-admin/quotas](https://console.cloud.s3nscloud.fr/iam-admin/quotas).

| 
|












| 

## Methods
| 
|



| 


### `[get](/docs/quotas/reference/rest/v1/organizations.locations.services.quotaInfos/get)`
| 

Retrieve the QuotaInfo of a quota for a project, folder or organization. | 
|

| 


### `[list](/docs/quotas/reference/rest/v1/organizations.locations.services.quotaInfos/list)`
| 

Lists QuotaInfos of all quotas for a given project, folder or organization. | 
|