# Method: organizations.locations.quotaPreferences.patch

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/organizations.locations.quotaPreferences/patch
Last updated: 2025-12-10

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












# Method: organizations. locations. quota Preferences. patch 






- On this page 
- [ HTTP request ](#http-request)
- [ Path parameters ](#path-parameters)
- [ Query parameters ](#query-parameters)
- [ Request body ](#request-body)
- [ Response body ](#response-body)
- [ Authorization scopes ](#authorization-scopes)
- [ IAM Permissions ](#iam-permissions)
- 















- [HTTP request](#body.HTTP_TEMPLATE)

- [Path parameters](#body.PATH_PARAMETERS)

- [Query parameters](#body.QUERY_PARAMETERS)

- [Request body](#body.request_body)

- [Response body](#body.response_body)

- [Authorization scopes](#body.aspect)

- [IAM Permissions](#body.aspect_1)

- [Try it!](#try-it)






Updates the parameters of a single QuotaPreference. It can updates the config in any states, not just the ones pending approval.






### HTTP request 



`PATCH https://cloudquotas.apis-berlin-build0.goog/v1/{quotaPreference.name=organizations/*/locations/*/quotaPreferences/*}`

The URL uses [gRPC Transcoding](https://google.aip.dev/127) syntax.




### Path parameters 








| 
Parameters | 
|



| 
`quota Preference. name` | 



`string`



Required except in the CREATE requests. The resource name of the quota preference. The path that follows `/locations` must be `/global`. For example: `projects/123/locations/global/quotaPreferences/my-config-for-us-east1`

| 
|





### Query parameters








| 
Parameters | 
|



| 
`update Mask` | 



`string ([FieldMask](https://apis-berlin-build0.goog/docs/discovery/type-format) format)`



Optional. Field mask is used to specify the fields to be overwritten in the QuotaPreference resource by the update. The fields specified in the updateMask are relative to the resource, not the full request. A field will be overwritten if it is in the mask. If the user does not provide a mask then all fields will be overwritten.

This is a comma-separated list of fully qualified names of fields. Example: `"user.displayName,photo"`.

| 
|

| 
`allow Missing` | 



`boolean`



Optional. If set to true, and the quota preference is not found, a new one will be created. In this situation, `updateMask` is ignored.

| 
|

| 
`validate Only` | 



`boolean`



Optional. If set to true, validate the request, but do not actually update. Note that a request being valid does not mean that the request is guaranteed to be fulfilled.

| 
|

| 
`ignore Safety Checks[]` | 



`enum ( [QuotaSafetyCheck](/docs/quotas/reference/rest/v1/QuotaSafetyCheck)`) 



The list of quota safety checks to be ignored.

| 
|





### Request body



The request body contains an instance of `[QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`.




### Response body



If successful, the response body contains an instance of `[QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`.




### Authorization scopes



Requires the following OAuth scope:




- `https://www.googleapis.com/auth/cloud-platform`


For more information, see the [Authentication Overview](/docs/authentication#authorization-gcp).




### IAM Permissions



Requires the following [IAM](https://berlin.devsitetest.how/iam/docs) permission on the `name` resource:




- `cloudquotas.quotas.update`


For more information, see the [IAM documentation](https://berlin.devsitetest.how/iam/docs).