# Campaigns

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /affiliate/campaigns | Get all the campaigns |
| GET | /affiliate/campaigns/{campaignId} | Get info about a specific campaign |

## Request Parameters \(For All Campaign fetch Endpoint\)

| Key | Value | Description | Required |
| :--- | :--- | :--- | :--- |
| limit | integer | The number of records to be displayed | Yes |
| page | integer | page number for the given limit | Yes |
| status | string | To fetch permission campaigns pass this key with value "requestPermission" | No |
| model | string | cpi, cpa, cpl, cps, cpc, cpm \(Any One\) | No |

## **All Campaigns**

### **Sample Request**

```bash
curl -H "X-Api-Key: {key}" "https://api.vnative.com/affiliate/campaigns"
```

#### Pagination

* Client needs to send the page number in the URL query parameter
* By default the first page is loaded with 10 campaigns
* You can load more campaigns by changing the limit like: &limit=100
* Keep on hitting the feed till there are no campaigns returned by the API

Sample Request with pagination

```text
curl 'https://api.vnative.com/affiliate/campaigns?apiKey={key}&limit=100&page=x'
```

_**Note: Feed will only display the active campaigns/offers. All the offers having tracking URL will be runnable by the affiliate**_

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "campaigns": [
            {
                "user_id": null,
                "display_id": 95,
                "org_id": "57c4718434243dc47d8b456b",
                "title": "Test Campaign",
                "description": "desc",
                "url": null,
                "preview_url": "http://preview-url",
                "image": null,
                "category": [
                    "Entertainment "
                ],
                "type": "article",
                "comm_type": "default",
                "device": [
                    "all"
                ],
                "os": ["android", "ios"],
                "os_ver": {
                  "android": {
                    "min": 5,
                    "max": 10
                  },
                  "ios": {
                    "min": 6,
                    "max": 12
                  }
                },
                "expiry": null,
                "deleted": false,
                "_id": "59f5e54cb6920d5b8a343c29",
                "live": true,
                "created": "2017-10-29",
                "modified": "2017-11-22",
                "meta": {
                    "pixel_tracking": "1",
                    "traffic": "ip_cookie",
                    "smart_link": true,
                    "cookie_lifetime": "365",
                    "conversion_cap_expire": false,
                    "click_cap_expire": false,
                    "impression_cap_expire": false
                },
                "status": "active",
                "commissions": [
                    {
                        "rate": 0.45,
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpa",
                        "description": null,
                        "ad_id": "59f5e54cb6920d5b8a343c29"
                    }
                ],
                "tracking_link": {
                    "url": "http://trk.vnative.com/{id}",
                    "live": true
                },
                "impressionUrl": "http://internal.gotrackier.com/imp?campaign_id=95&pub_id=3",
                "creatives": [],
                "bot_check_url": "http://14235.bot.ninja.com/imp?http://trk.vnative.com/{id}",
                "goals": [
                    {
                        "id": "5ce689b2b6920d0a303633f4",
                        "title": "Public Goal",
                        "value": "pub_goal",
                        "model": "fixed",
                        "payouts": [
                            {
                                "coverage": [
                                    "ALL"
                                ],
                                "payout": 8
                            }
                        ]
                    },
                    {
                        "id": "5ce68976b6920d0a303633eb",
                        "title": "Publisher Specific",
                        "value": "pub_specific",
                        "model": "percentage",
                        "payouts": [
                            {
                                "coverage": [
                                    "ALL"
                                ],
                                "payout": 700
                            }
                        ]
                    }
                ]
            },
            {...}
        ],
        "total": 40,
        "page": 1,
        "domains": [
            "trk.vnative.com",
            "sa.vnative.net"
        ]
    }
}
```

## **Single Campaign**

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" "https://api.vnative.com/affiliate/campaigns/58551c30b6920d760817f711"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "campaign": {
            "org_id": "string",
            "title": "Let's Barter - Android Apps on Google Play",
            "description": "Barter your Goods and Services and connect with individuals around you.",
            "preview_url": "https://play.google.com/store/apps/details?id=com.letsbarterindia.app",
            "creative": null,
            "image": "586ca5d.jpg",
            "category": [
                "Technology"
            ],
            "type": "article",
            "device": [
                "all"
            ],
            "os": ["android", "ios"],
            "os_ver": {
                  "android": {
                    "min": 5,
                    "max": 10
                  },
                  "ios": {
                    "min": 6,
                    "max": 12
                  }
            },
            "expiry": null,
            "_id": "{id}",
            "live": true,
            "created": "2017-01-05",
            "modified": "2017-01-15",
            "meta": {
                "permission": true
            }
        },
        "commissions": [
            {
                "rate": "0.1",
                "coverage": [
                    "ALL"
                ],
                "model": "cpi",
                "description": null
            }
        ],
        "tracking_link": {
            "url": "http://trk.vnative.com/{linkId}",
            "live": false
        },
        "impressionUrl": "http://internal.gotrackier.com/imp?campaign_id=3&pub_id=3",
        "permission": {
            "hasPermission": false,
            "permRequired": true,
            "access": {
                "_id": "589067e9b6920d1bd87b9ba3",
                "live": false
            }
        },
        "domains": [
            "dobolly.com"
        ]
    }
}
```

