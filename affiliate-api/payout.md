## **Get Payout**

| **HTTP method** | **End Point** |
| --- | --- |
| GET | /affiliate/payout |

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: d3207254-2036-012c-5c67-6770cb7db165" "https://api.vnative.com/affiliate/payout"
```

| Key | Type | Description | Nullable |
| --- | --- | --- | --- |
| start | date \(Y-m-d\) | Start date from which the stats should be displayed | Yes |
| end | date \(Y-m-d\) | End date till which the stats should be displayed | Yes |


### **Response body**

```json
{
    "success": true,
    "data": {
        "user": {
            "org_id": "string",
            "username": "demo",
            "name": "demo",
            "email": "demo@vnative.com",
            "password": "8c6a191eb2f4a7b29ff0b70202c5bb7c9264a5e0",
            "phone": null,
            "country": "IN",
            "currency": "USD",
            "type": "publisher",
            "login": "2016-12-16",
            "region": null,
            "_id": "string",
            "live": true,
            "created": "2016-12-16",
            "modified": "2016-12-23",
            "meta": []
        },
        "stats": {
            "2016-12-21": {
                "meta": {
                    "device": {
                        "desktop": 22
                    },
                    "os": {
                        "Mac OS": 17,
                        "Mac OS X": 3,
                        "Windows 7": 1,
                        "Windows 10": 1
                    },
                    "referer": {
                        "blogslog.in": 17,
                        "Empty": 3,
                        "l.facebook.com": 1,
                        "www.facebook.com": 1
                    },
                    "country": {
                        "US": 11,
                        "IN": 11
                    }
                },
                "clicks": 22,
                "impressions": 0,
                "conversions": 0,
                "payout": 3.722122
            },
            "2016-12-23": {
                "meta": {
                    "device": {
                        "desktop": 3
                    },
                    "os": {
                        "Linux": 3
                    },
                    "referer": {
                        "Empty": 2,
                        "blogslog.in": 1
                    },
                    "country": {
                        "IN": 3
                    }
                },
                "clicks": 3,
                "impressions": 0,
                "conversions": 1,
                "payout": 0.1
            },
            "2016-12-24": {
                "meta": {
                    "device": {
                        "desktop": 7,
                        "mobile": 3
                    },
                    "os": {
                        "Mac OS X": 4,
                        "Android": 3,
                        "Linux": 1,
                        "Mac OS": 1,
                        "Windows": 1
                    },
                    "referer": {
                        "Empty": 8,
                        "blogslog.in": 2
                    },
                    "country": {
                        "IN": 8,
                        "Empty": 2
                    }
                },
                "clicks": 10,
                "impressions": 0,
                "conversions": 4,
                "payout": 0.415
            },
            "2016-12-25": {
                "meta": {
                    "device": {
                        "desktop": 1
                    },
                    "os": {
                        "Mac OS": 1
                    },
                    "referer": {
                        "blogslog.in": 1
                    },
                    "country": {
                        "IN": 1
                    }
                },
                "clicks": 1,
                "impressions": 0,
                "conversions": 0,
                "payout": 0
            }
        },
        "total": {
            "meta": {
                "device": {
                    "desktop": 33,
                    "mobile": 3
                },
                "os": {
                    "Mac OS": 19,
                    "Mac OS X": 7,
                    "Windows 7": 1,
                    "Windows 10": 1,
                    "Linux": 4,
                    "Android": 3,
                    "Windows": 1
                },
                "referer": {
                    "blogslog.in": 21,
                    "Empty": 13,
                    "l.facebook.com": 1,
                    "www.facebook.com": 1
                },
                "country": {
                    "US": 11,
                    "IN": 23,
                    "Empty": 2
                }
            },
            "clicks": 36,
            "impressions": 0,
            "conversions": 5,
            "payout": 4.237122
        }
    }
}
```