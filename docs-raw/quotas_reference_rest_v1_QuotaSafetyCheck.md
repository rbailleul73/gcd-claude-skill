# QuotaSafetyCheck

Source: https://berlin.devsitetest.how/docs/quotas/reference/rest/v1/QuotaSafetyCheck
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












# Quota Safety Check 



















Enumerations of quota safety checks.










| 
Enums | 
|



| 
`QUOTA_ SAFETY_ CHECK_ UNSPECIFIED` | 
Unspecified quota safety check. | 
|

| 
`QUOTA_ DECREASE_ BELOW_ USAGE` | 
Validates that a quota mutation would not cause the consumer's effective limit to be lower than the consumer's quota usage. | 
|

| 
`QUOTA_ DECREASE_ PERCENTAGE_ TOO_ HIGH` | 
Validates that a quota mutation would not cause the consumer's effective limit to decrease by more than 10 percent. | 
|