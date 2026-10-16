# Method: organizations.locations.services.quotaInfos.get

Source: https://documentation.s3ns.fr/docs/quotas/reference/rest/v1/organizations.locations.services.quotaInfos/get
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



`GET https://cloudquotas.s3nsapis.fr/v1/{name=organizations/*/locations/*/services/*/quotaInfos/*}`

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



Requires the following [IAM](https://documentation.s3ns.fr/iam/docs) permission on the `name` resource:




- `cloudquotas.quotas.get`


For more information, see the [IAM documentation](https://documentation.s3ns.fr/iam/docs).