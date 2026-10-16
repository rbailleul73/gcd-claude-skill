# REST Resource: projects.locations.quotaPreferences

Source: https://documentation.s3ns.fr/docs/quotas/reference/rest/v1/projects.locations.quotaPreferences
Last updated: 2025-12-10

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












# REST Resource: projects. locations. quota Preferences 






- On this page 
- [ Resource: QuotaPreference ](#resource:-quotapreference)
- [ Methods ](#methods)

- [ create ](#create)
- [ get ](#get)
- [ list ](#list)
- [ patch ](#patch)

- 















- [Resource: QuotaPreference](#QuotaPreference)



- [JSON representation](#QuotaPreference.SCHEMA_REPRESENTATION)





- [Methods](#METHODS_SUMMARY)





## Resource: Quota Preference 




QuotaPreference represents the preferred quota configuration specified for a project, folder or organization. There is only one QuotaPreference resource for a quota value targeting a unique set of dimensions.






| 
JSON representation | 
|



| 

```
{ 
"name" : string , 
"dimensions" : { 
string : string , 
... 
} , 
"quotaConfig" : { 
object (`[QuotaConfig](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference.QuotaConfig)`) 
} , 
"etag" : string , 
"createTime" : string , 
"updateTime" : string , 
"service" : string , 
"quotaId" : string , 
"reconciling" : boolean , 
"justification" : string , 
"contactEmail" : string 
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



Required except in the CREATE requests. The resource name of the quota preference. The path that follows `/locations` must be `/global`. For example: `projects/123/locations/global/quotaPreferences/my-config-for-us-east1`

| 
|

| 
`dimensions` | 



`map (key: string, value: string)`



Immutable. The dimensions that this quota preference applies to. The key of the map entry is the name of a dimension, such as `region`, `zone`, `network_id`, and the value of the map entry is the dimension value.

If a dimension is missing from the map of dimensions, the quota preference applies to all the dimension values except for those that have other quota preferences configured for the specific value.

Note: QuotaPreferences can only be applied across all values of `user` and `resource` dimension. Do not set values for `user` or `resource` in the dimension map.

For example: `{"provider" : "Example Organization"}` where `provider` is a service-specific quota dimension and `Example Organization` is the provider name.

An object containing a list of `"key": value` pairs. Example: `{ "name": "wrench", "mass": "1.3kg", "count": "3" }`.

| 
|

| 
`quotaConfig` | 



`object ( [QuotaConfig](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference.QuotaConfig)`) 



Required. Preferred quota configuration.

| 
|

| 
`etag` | 



`string`



Optional. The current etag of the quota preference. If an etag is provided on update and does not match the current server's etag of the quota preference, the request will be blocked and an ABORTED error will be returned. See [https://google.aip.dev/134#etags](https://google.aip.dev/134#etags) for more details on etags.

| 
|

| 
`createTime` | 



`string ([Timestamp](https://s3nsapis.fr/docs/discovery/type-format) format)`



Output only. Create time stamp

Uses RFC 3339, where generated output will always be Z-normalized and use 0, 3, 6 or 9 fractional digits. Offsets other than "Z" are also accepted. Examples: `"2014-10-02T15:01:23Z"`, `"2014-10-02T15:01:23.045123456Z"` or `"2014-10-02T15:01:23+05:30"`.

| 
|

| 
`updateTime` | 



`string ([Timestamp](https://s3nsapis.fr/docs/discovery/type-format) format)`



Output only. Update time stamp

Uses RFC 3339, where generated output will always be Z-normalized and use 0, 3, 6 or 9 fractional digits. Offsets other than "Z" are also accepted. Examples: `"2014-10-02T15:01:23Z"`, `"2014-10-02T15:01:23.045123456Z"` or `"2014-10-02T15:01:23+05:30"`.

| 
|

| 
`service` | 



`string`



Required. The name of the service to which the quota preference is applied.

| 
|

| 
`quotaId` | 



`string`



Required. The id of the quota to which the quota preference is applied. A quota name is unique in the service. For example, `CpusPerProjectPerRegion`

| 
|

| 
`reconciling` | 



`boolean`



Output only. Is the quota preference pending Google Cloud approval and fulfillment.

| 
|

| 
`justification` | 



`string`



The reason / justification for this quota preference.

| 
|

| 
`contactEmail` | 



`string`



Input only. An email address that can be used to contact the user, in case Google Cloud needs more information to make a decision before additional quota can be granted.

When requesting a quota increase, the email address is required. When requesting a quota decrease, the email address is optional. For example, the email address is optional when the `QuotaConfig.preferred_value` is smaller than the `QuotaDetails.reset_value`.

| 
|












| 

## Methods
| 
|



| 


### `[create](/docs/quotas/reference/rest/v1/projects.locations.quotaPreferences/create)`
| 

Creates a new QuotaPreference that declares the desired value for a quota. | 
|

| 


### `[get](/docs/quotas/reference/rest/v1/projects.locations.quotaPreferences/get)`
| 

Gets details of a single QuotaPreference. | 
|

| 


### `[list](/docs/quotas/reference/rest/v1/projects.locations.quotaPreferences/list)`
| 

Lists QuotaPreferences in a given project, folder or organization. | 
|

| 


### `[patch](/docs/quotas/reference/rest/v1/projects.locations.quotaPreferences/patch)`
| 

Updates the parameters of a single QuotaPreference. | 
|