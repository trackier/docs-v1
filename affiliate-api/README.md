# **Affiliate API**

### **Available methods**

| **Operation** | **HTTP Method** | **End Point** | **Description** |
| --- | --- | --- | --- |
| Payout |  |  |  |
|  | GET | [/affiliate/payout](./payout.md) | Get payout details |
| Campaigns |  |  |  |
|  | GET | [/affiliate/campaigns](./campaigns.md) | Get all the campaigns |
|  | GET | [/affiliate/campaigns/{id}](./campaigns.md) | Get info about single campaign |
| Link |  |  |  |
|  | GET | [/affiliate/link/{campaignId}](./link.md) | Get the link for a campaign |
| Report |  |  |  |
|  | GET | [/affiliate/report](./report.md) | Get the date wise report |
|  | GET | [/affiliate/customReport](./custom-report.md) | Get customized report |
| Account |  |  |  |
|  | GET | [/affiliate/account](./account.md) | Get account info |
|  | PATCH | [/affiliate/account](./account.md) | Update account info |
| Campaign Access |  |  |  |
|  | POST | [/affiliate/requestAccess/{campaignId}](./request-access.md) | Request Access for a campaign which requires permission to run |
| Campaign Search |  |  |  |
|  | GET | [/affiliate/campaign-search](//affiliate-api/campaign-search.md) | Search Campaigns |



