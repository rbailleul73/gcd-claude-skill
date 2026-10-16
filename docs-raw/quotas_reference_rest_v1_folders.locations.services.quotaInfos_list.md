# Method: folders.locations.services.quotaInfos.list

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos/list
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












# Method: folders. locations. services. quota Infos. list 






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






Lists QuotaInfos of all quotas for a given project, folder or organization.






### HTTP request 



`GET https://cloudquotas.apis-berlin-build0.goog/v1/{parent=folders/*/locations/*/services/*}/quotaInfos`

The URL uses [gRPC Transcoding](https://google.aip.dev/127) syntax.




### Path parameters 








| 
Parameters | 
|



| 
`parent` | 



`string`



Required. Parent value of QuotaInfo resources. Listing across different resource containers (such as 'projects/-') is not allowed.

Example names: `projects/123/locations/global/services/compute.googleapis.com` `folders/234/locations/global/services/compute.googleapis.com` `organizations/345/locations/global/services/compute.googleapis.com`

| 
|





### Query parameters








| 
Parameters | 
|



| 
`page Size` | 



`integer`



Optional. Requested page size. Server may return fewer items than requested. If unspecified, server will pick an appropriate default.

| 
|

| 
`page Token` | 



`string`



Optional. A token identifying a page of results the server should return.

| 
|





### Request body



The request body must be empty.




### Response body



If successful, the response body contains an instance of `[ListQuotaInfosResponse](/docs/quotas/reference/rest/v1/ListQuotaInfosResponse)`.




### Authorization scopes



Requires the following OAuth scope:




- `https://www.googleapis.com/auth/cloud-platform`


For more information, see the [Authentication Overview](/docs/authentication#authorization-gcp).




### IAM Permissions



Requires the following [IAM](https://berlin.devsitetest.how/iam/docs) permission on the `parent` resource:




- `cloudquotas.quotas.get`


For more information, see the [IAM documentation](https://berlin.devsitetest.how/iam/docs).