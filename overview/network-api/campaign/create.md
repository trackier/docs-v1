# Create a New Campaign

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /campaign |

## **Request body example**

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: cc5d7610-80aa-8f1b-983d-fc5712fcfb53" -d '{
  "title": "API Campaign",
  "description": "This is a test campaign created using API",
  "preview_url": "http://google.com/",
  "url": "http://www.google.co.in/?utm_source={click_id}",
  "advertiser_id": "3",
  "status": "pending",
  "category": ["Technology", "Entertainment"],
  "currency": "USD",
  "model": "cpa",
  "os": ["android","ios"],
  "os_ver": {
    "android": {
      "min": 4,
      "max": 10
    }
  }
  "commissions": [
    {
      "payout": 1,
      "revenue": 2,
      "coverage": ["US", "IN"]
    },
    {
      "payout": 0.5,
      "revenue": 1,
      "coverage": ["ALL"]
    }
  ],
  "caps": [
        {
            "type":"revenue",
            "monthly": 30,
            "daily": 1,
            "lifetime":10000,
            "pc": 0,
            "pub_id": "5c9dca40b6920d57e15f1aa0",
            "geo": [
                "US", 
                "IN"    
            ]
        }
    ]
}' "https://api.vnative.com/campaign"
```

## **Request body parameters**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title\* | string | Title of the campaign | No |
| description | string | Description of the campaign | Yes |
| url\* | string | Url of the campaign | No |
| image | string | Url of the image \(which is downloadable\) | Yes |
| preview\_url | string | Preview URL of campaign | Yes |
| device | array | Device array | Yes |
| os | array | Operating System \(all/android/ios\) | Yes |
| os\_ver | object | Operating System Version Info | Yes |
| category | array | Categories array | Yes |
| advertiser\_id\* | string | Advertiser ID | No |
| commissions\* | array of objects | Campaign Commissions | No |
| caps | array of objects | Campaign CAPs | Yes |
| model\* | string | CPA, CPC, CPI, CPM \(default: CPA\) | No |
| currency | string | 3 letter currency code \(example: USD\) | Yes |
| status | string | active, pending, paused, disabled \(default: pending\) | Yes |
| visibility | string | public, private, permission \(default: public\) | Yes |
| app\_name | string | App Name for campaign | Yes |
| app\_id | string | App ID of campaign | Yes |
| conversion\_tracking | string | postback, iframe\_https, image\_https \(default: postback\) | Yes |
| conversion\_pixel\_domain | string | pixel domain required when conversion tracking is not postback | Yes |

### **Commission Object**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| payout\* | float | Payout for the affiliate in Admin Currency \(default: USD\) | No |
| revenue\* | float | Revenue charged from the advertiser Admin Currency \(default: USD\) | No |
| coverage | array | Array of country codes | Yes |

* User ID can be found from /advertiser
* Fields marked with \* are required

### **CAP Object**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">type</th>
      <th style="text-align:left">string</th>
      <th style="text-align:left">
        <ul>
          <li>conversion</li>
          <li>payout</li>
          <li>revenue</li>
          <li>click</li>
          <li>pendingPayout</li>
          <li>pendingRevenue</li>
          <li>approvedConv</li>
        </ul>
      </th>
      <th style="text-align:left">No</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| pub\_id \(Deprecated\) | string | Publisher Long ID | Yes |
| :--- | :--- | :--- | :--- |


| pids | array | Publisher ID's | No |
| :--- | :--- | :--- | :--- |


| daily | integer | Daily CAP limit | Yes |
| :--- | :--- | :--- | :--- |


| monthly | integer | Monthly CAP Limit | Yes |
| :--- | :--- | :--- | :--- |


| lifetime | integer | Lifetime CAP Limit | Yes |
| :--- | :--- | :--- | :--- |


| pc | integer | 0 - false/1 - true | Yes |
| :--- | :--- | :--- | :--- |


| geo | array | List of country codes | Yes |
| :--- | :--- | :--- | :--- |


```javascript
{
    "success": true,
    "data": {
        "campaign": {
            "user_id": "57c4738434243dc57d8b456d",
            "org_id": "57c4718434243dc47d8b456b",
            "display_id": 1807,
            "title": "API Campaign 5",
            "description": "This is a test campaign created using API",
            "url": "http://www.google.co.in/?utm_source={click_id}",
            "preview_url": "http://google.com/",
            "image": null,
            "os":["all"],
            "os_ver": null,
            "category": [
                "Technology",
                "Entertainment"
            ],
            "currency": "USD",
            "comm_model": "cpa",
            "comm_type": "default",
            "device": null,
            "coverage": [
                "US",
                "IN",
                "ALL"
            ],
            "fire_global_aff_pb": true,
            "os": [],
            "os_ver": null,
            "cities": [],
            "isps": [],
            "disabled_reason": null,
            "blocked_pubs": [],
            "fallback_url": null,
            "cookie_duration": 90,
            "app_name": null,
            "app_id": null,
            "def_goal": null,
            "conv_tracking": "postback",
            "convt_domain": null,
            "vis": "private",
            "cdt": null,
            "_id": "5bebd18b89d44647667249f2",
            "live": true,
            "created": "2018-11-14",
            "modified": "2018-11-14",
            "meta": {},
            "status": "active"
        },
        "commissions": [
            {
                "ad_id": "5bebd18b89d44647667249f2",
                "tier_id": null,
                "rate": 1,
                "revenue": 2,
                "coverage": [
                    "US",
                    "IN"
                ],
                "_id": "5bebd18c89d44647667249f3"
            },
            {
                "ad_id": "5bebd18b89d44647667249f2",
                "tier_id": null,
                "rate": 0.5,
                "revenue": 1,
                "coverage": [
                    "ALL"
                ],
                "_id": "5bebd18c89d44647667249f4"
            }
        ],
        "caps": [
            {
                "pub_id": "ALL",
                "ad_id": "5ca567dadc713839091cc064",
                "type": "conversion",
                "redirect": {
                    "type": "fallback_link"
                },
                "geo": [
                    "US"
                ],
                "id": "5ca567dadc713839091cc067",
                "daily": null,
                "monthly": 10,
                "lifetime": null,
                "pause_campaign": 1
            }
        ],
        "message": "Campaign created Successfully!!"
    }
}
```

