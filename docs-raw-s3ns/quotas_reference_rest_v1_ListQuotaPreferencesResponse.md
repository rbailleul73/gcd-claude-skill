# ListQuotaPreferencesResponse

Source: https://documentation.s3ns.fr/docs/quotas/reference/rest/v1/ListQuotaPreferencesResponse
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












# List Quota Preferences Response 



















- [JSON representation](#SCHEMA_REPRESENTATION)





Message for response to listing QuotaPreferences






| 
JSON representation | 
|



| 

```
{ 
"quotaPreferences" : [ 
{ 
object (`[QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`) 
} 
] , 
"nextPageToken" : string , 
"unreachable" : [ 
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
`quota Preferences[]` | 



`object ( [QuotaPreference](/docs/quotas/reference/rest/v1/folders.locations.quotaPreferences#QuotaPreference)`) 



The list of QuotaPreference

| 
|

| 
`next Page Token` | 



`string`



A token, which can be sent as `pageToken` to retrieve the next page. If this field is omitted, there are no subsequent pages.

| 
|

| 
`unreachable[]` | 



`string`



Locations that could not be reached.

| 
|