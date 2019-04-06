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
                "creatives": []
            },
            {...}
        ],
        "total": 40,
        "page": 1,
        "private_campaigns": [
            {
                "user_id": null,
                "display_id": 85,
                "org_id": "57c4718434243dc47d8b456b",
                "title": "LOAD TEST",
                "description": null,
                "url": null,
                "preview_url": "https://requestb.in/1erd44h1",
                "image": "59a95775b43f9.png",
                "category": [
                    "Technology"
                ],
                "type": null,
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
                "_id": "59a95776b6920d1df631282f",
                "live": true,
                "created": "2017-09-01",
                "modified": "2017-11-04",
                "meta": {
                    "conversion_cap_expire": false,
                    "click_cap_expire": false,
                    "impression_cap_expire": false,
                    "pixel_tracking": "1",
                    "traffic": "ip_cookie",
                    "smart_link": true,
                    "cookie_lifetime": "365",
                    "private": true
                },
                "status": "active",
                "commissions": [
                    {
                        "rate": 0.015151515151515,
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpa",
                        "description": null,
                        "ad_id": "59a95776b6920d1df631282f"
                    }
                ],
                "tracking_link": {
                    "url": "http://trk.vnative.com/{id}",
                    "live": true
                },
                "impressionUrl": "http://internal.gotrackier.com/imp?campaign_id=3&pub_id=3",
                "creatives": [
                    {
                        "ad_id": "59a95776b6920d1df631282f",
                        "dimensions": {
                            "width": 1417,
                            "height": 348
                        },
                        "name": "59f9aed8f3332.png",
                        "title": "2",
                        "type": "image/png",
                        "crtv_type": null,
                        "_id": "59f9aed9b6920d40ab34ada3",
                        "meta": {},
                        "created": "2017-11-01"
                    }
                ]
            },
            {
                "user_id": null,
                "display_id": 17,
                "org_id": "57c4718434243dc47d8b456b",
                "title": "Tracking Image – Plan Your Tours",
                "description": null,
                "url": null,
                "preview_url": "http://planyourtours.com/product/tracking-image/",
                "image": "586a9073193af.png",
                "category": [
                    "Technology"
                ],
                "type": null,
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
                "_id": "586a9073b6920d26411ade98",
                "live": true,
                "created": "2017-01-02",
                "modified": "2017-06-14",
                "meta": {
                    "traffic": "ip_cookie",
                    "private": true,
                    "pixel_tracking": "1"
                },
                "status": "active",
                "commissions": [
                    {
                        "rate": 4,
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpa",
                        "description": null,
                        "ad_id": "586a9073b6920d26411ade98"
                    }
                ],
                "tracking_link": {
                    "url": "http://trk.vnative.com/{id}",
                    "live": true
                },
                "impressionUrl": "http://internal.gotrackier.com/imp?campaign_id=3&pub_id=3",
                "creatives": [
                    {
                        "ad_id": "586a9073b6920d26411ade98",
                        "dimensions": [],
                        "name": "5a0961faa94b1.html",
                        "title": "Emailer 10",
                        "type": "text/html",
                        "crtv_type": "email",
                        "_id": "5a0961fbb6920d1de775aecd",
                        "meta": {
                            "relatedFiles": [
                                {
                                    "name": "Untitled.jpg",
                                    "uploaded": "5a0961fb2cbe8.jpg"
                                }
                            ]
                        },
                        "created": "2017-11-13"
                    }
                ]
            }
        ],
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

