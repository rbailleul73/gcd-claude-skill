# Method: folders.locations.quotaPreferences.get

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences/get
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












# Method: folders. locations. quota Preferences. get 






- On this page 
- [ HTTP request ](#http-request)
- [ Path parameters ](#path-parameters)
- [ Request body ](#request-body)
- [ Response body ](#response-body)
- [ Authorization scopes ](#authorization-scopes)
- [ IAM Permissions ](#iam-permissions)
- 















- [HTTP request](#body.HTTP_TEMPLATE)

- [Path parameters](#body.PATH_PARAMETERS)

- [Request body](#body.request_body)

- [Response body](#body.response_body)

- [Authorization scopes](#body.aspect)

- [IAM Permissions](#body.aspect_1)

- [Try it!](#try-it)






Gets details of a single QuotaPreference.






### HTTP request 



`GET https://cloudquotas.apis-berlin-build0.goog/v1/{name=folders/*/locations/*/quotaPreferences/*}`

The URL uses [gRPC Transcoding](https://google.aip.dev/127) syntax.




### Path parameters 








| 
Parameters | 
|



| 
`name` | 



`string`



Required. Name of the resource

Example name: `projects/123/locations/global/quotaPreferences/my-config-for-us-east1`

| 
|





### Request body



The request body must be empty.




### Response body



If successful, the response body contains an instance of `[QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`.




### Authorization scopes



Requires the following OAuth scope:




- `https://www.googleapis.com/auth/cloud-platform`


For more information, see the [Authentication Overview](/docs/authentication#authorization-gcp).




### IAM Permissions



Requires the following [IAM](https://berlin.devsitetest.how/iam/docs) permission on the `name` resource:




- `cloudquotas.quotas.get`


For more information, see the [IAM documentation](https://berlin.devsitetest.how/iam/docs).