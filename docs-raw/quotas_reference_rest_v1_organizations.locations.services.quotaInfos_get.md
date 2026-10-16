# Method: organizations.locations.services.quotaInfos.get

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/organizations.locations.services.quotaInfos/get
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












# Method: organizations. locations. services. quota Infos. get 






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






Retrieve the QuotaInfo of a quota for a project, folder or organization.






### HTTP request 



`GET https://cloudquotas.apis-berlin-build0.goog/v1/{name=organizations/*/locations/*/services/*/quotaInfos/*}`

The URL uses [gRPC Transcoding](https://google.aip.dev/127) syntax.




### Path parameters 








| 
Parameters | 
|



| 
`name` | 



`string`



Required. The resource name of the quota info.

An example name: `projects/123/locations/global/services/compute.googleapis.com/quotaInfos/CpusPerProjectPerRegion`

| 
|





### Request body



The request body must be empty.




### Response body



If successful, the response body contains an instance of `[QuotaInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo)`.




### Authorization scopes



Requires the following OAuth scope:




- `https://www.googleapis.com/auth/cloud-platform`


For more information, see the [Authentication Overview](/docs/authentication#authorization-gcp).




### IAM Permissions



Requires the following [IAM](https://berlin.devsitetest.how/iam/docs) permission on the `name` resource:




- `cloudquotas.quotas.get`


For more information, see the [IAM documentation](https://berlin.devsitetest.how/iam/docs).