# **Advertiser Report**

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /advertiser/campaignStats/{id} | Get Day wise stats for a campaign |

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 3c25dbcc-806a-b87f-5f29-338b74d04709" "https://api.vnative.com/advertiser/campaignStats/{id}"
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
        "stats": {
            "2017-02-07": {
                "clicks": 3,
                "impressions": 0,
                "conversions": 0,
                "revenue": 0,
                "payout": 0,
                "meta": {
                    "device": {
                        "mobile": 2,
                        "desktop": 1
                    },
                    "os": {
                        "Android": 2,
                        "Mac OS X": 1
                    },
                    "referer": {
                        "Empty": 3
                    },
                    "country": {
                        "US": 2,
                        "IN": 1
                    }
                }
            },
            "2017-02-08": {
                "clicks": 5,
                "impressions": 0,
                "conversions": 1,
                "revenue": 0.15,
                "payout": 0.1,
                "meta": {
                    "device": {
                        "desktop": 4,
                        "mobile": 3
                    },
                    "os": {
                        "Android": 3,
                        "Windows 7": 2,
                        "Linux": 2
                    },
                    "referer": {
                        "Empty": 7
                    },
                    "country": {
                        "US": 4,
                        "IN": 2
                    }
                }
            }
        },
        "total": {
            "meta": {
                "device": {
                    "mobile": 5,
                    "desktop": 5
                },
                "os": {
                    "Android": 5,
                    "Mac OS X": 1,
                    "Windows 7": 2,
                    "Linux": 2
                },
                "referer": {
                    "Empty": 10
                },
                "country": {
                    "US": 6,
                    "IN": 3
                }
            },
            "clicks": 8,
            "impressions": 0,
            "conversions": 1,
            "revenue": 0.15,
            "payout": 0.1
        }
    }
}
```



