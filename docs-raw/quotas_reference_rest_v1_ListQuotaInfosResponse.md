# ListQuotaInfosResponse

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/ListQuotaInfosResponse
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