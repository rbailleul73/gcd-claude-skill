# ListQuotaPreferencesResponse

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/ListQuotaPreferencesResponse
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