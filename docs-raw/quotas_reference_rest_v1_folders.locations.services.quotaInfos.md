# REST Resource: folders.locations.services.quotaInfos

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos
Last updated: 2026-01-21

Some or all of the information on this page might not apply to Google Cloud Dedicated. See [Differences from Google Cloud](/docs/quotas/tpc-differences) for more details.














- 





[

Home

](https://berlin.devsitetest.how/)






- 








[

Documentation

](https://berlin.devsitetest.how/docs)






- 








[

Cloud Quotas

](https://berlin.devsitetest.how/docs/quotas)






- 








[

Reference

](https://berlin.devsitetest.how/docs/quotas/apis)












# REST Resource: folders. locations. services. quota Infos 






- On this page 
- [ Resource: QuotaInfo ](#resource:-quotainfo)

- [ ContainerType ](#containertype)
- [ QuotaIncreaseEligibility ](#quotaincreaseeligibility)
- [ IneligibilityReason ](#ineligibilityreason)
- [ DimensionsInfo ](#dimensionsinfo)
- [ QuotaDetails ](#quotadetails)
- [ RolloutInfo ](#rolloutinfo)

- [ Methods ](#methods)

- [ get ](#get)
- [ list ](#list)

- 















- [Resource: QuotaInfo](#QuotaInfo)



- [JSON representation](#QuotaInfo.SCHEMA_REPRESENTATION)

- [ContainerType](#QuotaInfo.ContainerType)

- [QuotaIncreaseEligibility](#QuotaInfo.QuotaIncreaseEligibility)



- [JSON representation](#QuotaInfo.QuotaIncreaseEligibility.SCHEMA_REPRESENTATION)





- [IneligibilityReason](#QuotaInfo.IneligibilityReason)

- [DimensionsInfo](#QuotaInfo.DimensionsInfo)



- [JSON representation](#QuotaInfo.DimensionsInfo.SCHEMA_REPRESENTATION)





- [QuotaDetails](#QuotaInfo.QuotaDetails)



- [JSON representation](#QuotaInfo.QuotaDetails.SCHEMA_REPRESENTATION)





- [RolloutInfo](#QuotaInfo.RolloutInfo)



- [JSON representation](#QuotaInfo.RolloutInfo.SCHEMA_REPRESENTATION)









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



URI to the page where users can request more quota for the cloud service—for example, [https://console.cloud.google.com/iam-admin/quotas](https://console.cloud.berlin-build0.goog/iam-admin/quotas).

| 
|





### ContainerType




The enumeration of the types of a cloud resource container.










| 
Enums | 
|



| 
`CONTAINER_TYPE_UNSPECIFIED` | 
Unspecified container type. | 
|

| 
`PROJECT` | 
consumer project | 
|

| 
`FOLDER` | 
folder | 
|

| 
`ORGANIZATION` | 
organization | 
|






### QuotaIncreaseEligibility




Eligibility information regarding requesting increase adjustment of a quota.






| 
JSON representation | 
|



| 

```
{ 
"isEligible" : boolean , 
"ineligibilityReason" : enum (`[IneligibilityReason](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.IneligibilityReason)`) 
} 
```
| 
|











| 
Fields | 
|



| 
`isEligible` | 



`boolean`



Whether a higher quota value can be requested for the quota.

| 
|

| 
`ineligibilityReason` | 



`enum ( [IneligibilityReason](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.IneligibilityReason)`) 



The reason of why it is ineligible to request increased value of the quota. If the isEligible field is true, it defaults to INELIGIBILITY_REASON_UNSPECIFIED.

| 
|






### IneligibilityReason




The enumeration of reasons when it is ineligible to request increase adjustment.










| 
Enums | 
|



| 
`INELIGIBILITY_REASON_UNSPECIFIED` | 
Default value when isEligible is true. | 
|

| 
`NO_VALID_BILLING_ACCOUNT` | 
The container is not linked with a valid billing account. | 
|

| 
`NOT_SUPPORTED` | 
Quota increase is not supported for the quota. | 
|

| 
`NOT_ENOUGH_USAGE_HISTORY` | 
There is not enough usage history to determine the eligibility. | 
|

| 
`OTHER` | 
Other reasons. | 
|






### DimensionsInfo




The detailed quota information such as effective quota value for a combination of dimensions.






| 
JSON representation | 
|



| 

```
{ 
"dimensions" : { 
string : string , 
... 
} , 
"details" : { 
object (`[QuotaDetails](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.QuotaDetails)`) 
} , 
"applicableLocations" : [ 
string 
] 
} 
```
| 
|











| 
Fields | 
|



| 
`dimensions` | 



`map (key: string, value: string)`



The map of dimensions in key-value pairs. The key of a map entry is "region", "zone", or the name of a service-specific dimension, and the value of a map entry is the value of the dimension. If a dimension does not appear in the map of dimensions, the dimensions info applies to all the dimension values except for those that have another DimensionInfo instance configured for the specific value. For example: `{"provider" : "Example Organization"}` where `provider` is a service-specific quota dimension and `Example Organization` is the provider name.

An object containing a list of `"key": value` pairs. Example: `{ "name": "wrench", "mass": "1.3kg", "count": "3" }`.

| 
|

| 
`details` | 



`object ( [QuotaDetails](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.QuotaDetails)`) 



Quota details for the specified dimensions.

| 
|

| 
`applicableLocations[]` | 



`string`



The applicable regions or zones of this dimension. The field is set to ['global'] for quotas that are not per region or per zone. Otherwise, it will be set to the list of locations this dimension info is applicable to.

| 
|






### QuotaDetails




The quota details for a map of dimensions.






| 
JSON representation | 
|



| 

```
{ 
"value" : string , 
"rolloutInfo" : { 
object (`[RolloutInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.RolloutInfo)`) 
} 
} 
```
| 
|











| 
Fields | 
|



| 
`value` | 



`string ([int64](https://apis-berlin-build0.goog/docs/discovery/type-format) format)`



The value currently in effect and being enforced.

| 
|

| 
`rolloutInfo` | 



`object ( [RolloutInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo.RolloutInfo)`) 



Rollout information of this quota. This field is present only if the effective limit will change due to the ongoing rollout of the service config.

| 
|






### RolloutInfo




[Output only] Rollout information of a quota.






| 
JSON representation | 
|



| 

```
{ 
"ongoingRollout" : boolean 
} 
```
| 
|











| 
Fields | 
|



| 
`ongoingRollout` | 



`boolean`



Whether there is an ongoing rollout for a quota or not.

| 
|













| 

## Methods
| 
|



| 


### `[get](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos/get)`
| 

Retrieve the QuotaInfo of a quota for a project, folder or organization. | 
|

| 


### `[list](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos/list)`
| 

Lists QuotaInfos of all quotas for a given project, folder or organization. | 
|