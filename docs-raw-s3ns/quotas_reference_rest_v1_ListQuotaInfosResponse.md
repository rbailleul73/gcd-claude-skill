# ListQuotaInfosResponse

Source: https://documentation.s3ns.fr/docs/quotas/reference/rest/v1/ListQuotaInfosResponse
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












# List Quota Infos Response 



















- [JSON representation](#SCHEMA_REPRESENTATION)





Message for response to listing QuotaInfos






| 
JSON representation | 
|



| 

```
{ 
"quotaInfos" : [ 
{ 
object (`[QuotaInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo)`) 
} 
] , 
"nextPageToken" : string 
} 
```
| 
|











| 
Fields | 
|



| 
`quota Infos[]` | 



`object ( [QuotaInfo](/docs/quotas/reference/rest/v1/folders.locations.services.quotaInfos#QuotaInfo)`) 



The list of QuotaInfo

| 
|

| 
`next Page Token` | 



`string`



A token, which can be sent as `pageToken` to retrieve the next page. If this field is omitted, there are no subsequent pages.

| 
|