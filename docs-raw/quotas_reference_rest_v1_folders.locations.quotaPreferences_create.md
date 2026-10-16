# Method: folders.locations.quotaPreferences.create

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences/create
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












# Method: folders. locations. quota Preferences. create 






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






Creates a new QuotaPreference that declares the desired value for a quota.






### HTTP request 



`POST https://cloudquotas.apis-berlin-build0.goog/v1/{parent=folders/*/locations/*}/quotaPreferences`

The URL uses [gRPC Transcoding](https://google.aip.dev/127) syntax.




### Path parameters 








| 
Parameters | 
|



| 
`parent` | 



`string`



Required. Value for parent.

Example: `projects/123/locations/global`

| 
|





### Query parameters








| 
Parameters | 
|



| 
`quota Preference Id` | 



`string`



Optional. Id of the requesting object, must be unique under its parent. If client does not set this field, the service will generate one.

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



If successful, the response body contains a newly created instance of `[QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`.




### Authorization scopes



Requires the following OAuth scope:




- `https://www.googleapis.com/auth/cloud-platform`


For more information, see the [Authentication Overview](/docs/authentication#authorization-gcp).




### IAM Permissions



Requires the following [IAM](https://berlin.devsitetest.how/iam/docs) permission on the `parent` resource:




- `cloudquotas.quotas.update`


For more information, see the [IAM documentation](https://berlin.devsitetest.how/iam/docs).