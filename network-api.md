# **Network API**

### **Available methods**

| **Operation** | **HTTP Method** | **End Point** | **Description** |
| --- | --- | --- | --- |
| Campaigns |  |  |  |
|  | GET | [/campaign](campaign/read.md) | Get all the campaigns |
|  | GET | [/campaign/stats/{id}](campaign/stats.md) | Get campaign stats |
|  | POST | [/campaign](campaign/create.md) | Create a new campaign |
|  | POST | [/campaign/{id}](campaign/edit.md) | Edit a campaign |
|  | DELETE | [/campaign/{id}](campaign/delete.md) | Remove any campaign |
|  | GET | [/commissions/{route}](campaign/commissions/README.md) | Commission Routes |
| Affiliate |  |  |  |
|  | GET | [/affiliate](affiliate/read.md) | Get all the affiliates |
|  | POST | [/affiliate](affiliate/create.md) | Create a new affiliate |
|  | POST | [/affiliate/{id}](affiliate/edit.md) | Edit an affiliate info |
|  | DELETE | [/affiliate/{id}](affiliate/delete.md) | Remove any affiliate |
| Advertiser |  |  |  |
|  | GET | [/advertiser](advertiser/read.md) | Get all the advertisers |
|  | POST | [/advertiser](advertiser/create.md) | Create a new advertiser |
|  | POST | [/advertiser/{id}](advertiser/edit.md) | Edit an advertiser info |
|  | DELETE | [/advertiser/{id}](advertiser/delete.md) | Remove any advertiser |
| Dictionary |  |  |  |
|  | GET | [/dict/{route}](dict/README.md) | Get Dictionary Routes |
| Operations |  |  |  |
|  | GET | [/network/account](network-ops/account.md) | Get Network Details |
|  | GET | [/network/stats](network-ops/stats.md) | Get Network stats |
|  | PATCH | [/network/account](network-ops/account.md) | Edit Network Details |
|  | GET | [/network/link/{affId}/{campaignId}](network-ops/tracking-link.md) | Get the tracking link for an affiliate |
|  | POST | [/network/link/{affId}/{campaignId}](network-ops/tracking-link.md) | Create a tracking link for an affiliate for a campaign |
|  | GET | [/network/conversions](network-ops/conversions.md) | Get Conversion Logs |
| Affiliate Referral Operations |  |  |  |
|  | GET | [/network/referral](network-ops/referral/read.md) | Get all the Referral Links |
|  | POST | [/network/referral](network-ops/referral/create.md) | Create a new referral link |
|  | PATCH | [/network/referral/{id}](network-ops/referral/edit.md) | Edit a referral link |
|  | DELETE | [/network/referral/{id}](network-ops/referral/delete.md) | Remove a referral link |


