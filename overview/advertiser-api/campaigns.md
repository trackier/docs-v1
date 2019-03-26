# Campaigns

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /advertiser/campaigns | Get all the campaigns |
| GET | /advertiser/campaigns/{campaignId} | Get info about a specific campaign |

## **All Campaigns**

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: f589a813-1ead-93b8-1af7-c57c74376a66" "https://api.vnative.com/advertiser/campaigns"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "campaigns": [
            {
                "user_id": "string",
                "org_id": "string",
                "title": "Traffic Arbitrage – Plan Your Tours",
                "description": null,
                "url": "http://planyourtours.com/product/traffic-arbitrage/?utm_source={aff_id}&utm_campaign={campaign_id}&utm_medium=affiliate&utm_content={click_id}",
                "preview_url": "http://planyourtours.com/product/traffic-arbitrage/",
                "creative": [],
                "image": "588f2c947e.png",
                "category": [
                    "Technology"
                ],
                "type": "article",
                "device": [
                    "all"
                ],
                "expiry": null,
                "_id": "string",
                "live": false,
                "created": "2017-01-30",
                "modified": null,
                "meta": [],
                "commissions": [
                    {
                        "revenue": "50 %",
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cps",
                        "description": null
                    }
                ]
            },
            {
                "user_id": "string",
                "org_id": "string",
                "title": "India Does Not Deserve Art And Artists. It's Not The Country It Once Was",
                "description": "There's no pride in protecting one's culture if that culture enables you to get violent.",
                "url": "http://beingindian.com/my-opinion/india-does-not-deserve-art/?utm_source={aff_id}&utm_campaign={campaign_id}&utm_medium=affiliate&utm_content={click_id}",
                "preview_url": "http://beingindian.com/my-opinion/india-does-not-deserve-art/",
                "creative": [],
                "image": "588cc44a85ad4.png",
                "category": [
                    "News"
                ],
                "type": "article",
                "device": [
                    "all"
                ],
                "expiry": "2017-02-04",
                "_id": "string",
                "live": false,
                "created": "2017-01-28",
                "modified": null,
                "meta": [],
                "commissions": [
                    {
                        "revenue": "9.9",
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpc",
                        "description": null
                    }
                ]
            },
            {
                "user_id": "string",
                "org_id": "string",
                "title": "How To Motivate Yourself To Stay Fit?",
                "description": "If you have recently worked hard to lose some pounds, you probably want to keep it that way. This guide will help you in maintaining your new earned physique for the rest",
                "url": "http://dailythoughts.xyz/how-to-motivate-yourself-to-stay-fit/",
                "preview_url": "http://dailythoughts.xyz/how-to-motivate-yourself-to-stay-fit/",
                "creative": null,
                "image": "5878848146947.jpeg",
                "category": [
                    "Sports",
                    "Lifestyle and food"
                ],
                "type": "article",
                "device": [
                    "all"
                ],
                "expiry": "2017-02-01",
                "_id": "string",
                "live": false,
                "created": "2017-01-25",
                "modified": "2017-01-31",
                "meta": [],
                "commissions": [
                    {
                        "revenue": "653.4",
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpc",
                        "description": null
                    },
                    {
                        "revenue": "66",
                        "coverage": [
                            "AU",
                            "CA",
                            "GB",
                            "US"
                        ],
                        "model": "cpc",
                        "description": null
                    },
                    {
                        "revenue": "66",
                        "coverage": [
                            "IN",
                            "PK"
                        ],
                        "model": "cpc",
                        "description": null
                    }
                ]
            },
            {
                "user_id": "string",
                "org_id": "string",
                "title": "Blogslogin Web Analysis - Blogslogin.com",
                "description": null,
                "url": "https://blogslogin.com.cutestat.com",
                "preview_url": "https://blogslogin.com.cutestat.com",
                "creative": null,
                "image": "58793aa0508f7.png",
                "category": [
                    "Technology"
                ],
                "type": "article",
                "device": [
                    "all"
                ],
                "expiry": "2017-02-01",
                "_id": "string",
                "live": false,
                "created": "2017-01-15",
                "modified": "2017-01-31",
                "meta": [],
                "commissions": [
                    {
                        "revenue": "9.9",
                        "coverage": [
                            "ALL",
                            "RU"
                        ],
                        "model": "cpa",
                        "description": "Successful acquisition would be when a form is submitted,newslater sign up, registration,an impression."
                    }
                ]
            },
            {
                "user_id": "string",
                "org_id": "string",
                "title": "InRead Video - vNative com - YouTube",
                "description": "See Live demo of Video Native Advertising Start your own affiliate network : https://goo.gl/SrnUkh",
                "url": "https://www.youtube.com/watch?v=FNroDGan3ws",
                "preview_url": "https://www.youtube.com/watch?v=FNroDGan3ws",
                "creative": [],
                "image": "5826cf67c56e4.jpeg",
                "category": [
                    "Technology"
                ],
                "type": "video",
                "device": [
                    "all"
                ],
                "expiry": null,
                "_id": "string",
                "live": false,
                "created": "2016-11-12",
                "modified": "2016-11-30",
                "meta": {
                    "videoUrl": "https://www.youtube.com/watch?v=FNroDGan3ws",
                    "videos": [
                        {
                            "file": "5826db1b672c9.mp4",
                            "quality": "240p"
                        },
                        {
                            "file": "5826db1dedcca.mp4",
                            "quality": "360p"
                        }
                    ]
                },
                "commissions": [
                    {
                        "revenue": "43.12K",
                        "coverage": [
                            "ALL"
                        ],
                        "model": "cpc",
                        "description": null
                    }
                ]
            }
        ],
        "total": 5,
        "page": 1
    }
}
```

## **Single Campaign**

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: c4fec290-5071-a7e3-678d-9f1aac32c768" "https://api.vnative.com/advertiser/campaigns/{campaignId}"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "campaign": {
            "user_id": "string",
            "org_id": "string",
            "title": "How To Motivate Yourself To Stay Fit?",
            "description": "If you have recently worked hard to lose some pounds, you probably want to keep it that way. This guide will help you in maintaining your new earned physique for the rest",
            "url": "http://dailythoughts.xyz/how-to-motivate-yourself-to-stay-fit/",
            "preview_url": "http://dailythoughts.xyz/how-to-motivate-yourself-to-stay-fit/",
            "creative": null,
            "image": "5878848147.jpeg",
            "category": [
                "Sports",
                "Lifestyle and food"
            ],
            "type": "article",
            "device": [
                "all"
            ],
            "expiry": "2017-02-01",
            "_id": "string",
            "live": false,
            "created": "2017-01-25",
            "modified": "2017-01-31",
            "meta": []
        },
        "commissions": [
            {
                "revenue": "653.4",
                "coverage": [
                    "ALL"
                ],
                "model": "cpc",
                "description": null
            },
            {
                "revenue": "66",
                "coverage": [
                    "AU",
                    "CA",
                    "GB",
                    "US"
                ],
                "model": "cpc",
                "description": null
            },
            {
                "revenue": "66",
                "coverage": [
                    "IN",
                    "PK"
                ],
                "model": "cpc",
                "description": null
            }
        ]
    }
}
```

