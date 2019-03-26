# Campaign stats

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /campaign/stats/{id} | Date wise stats for a campaign |
| GET | /campaign/stats/{id}/{affId} | Date wise stats of an affiliate for a campaign |

## GET Request Parameters

| Key | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| start | string | Start Date in YYYY-mm-dd format (Optional) | Yes |
| end | string | End Date in YYYY-mm-dd format (Optional) | Yes |

## Response body

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" https://api.vnative.com/campaign/stats/{id}
```

```json
 {
    "success": true,
    "data": {
        "stats": {
            "2017-01-14": {
                "clicks": 0,
                "impressions": 1,
                "conversions": 0,
                "revenue": 1.18,
                "payout": 0.35,
                "meta": {
                    "device": {
                        "mobile": 1
                    },
                    "os": [],
                    "referer": {
                        "blogslog.in": 1
                    },
                    "country": {
                        "US": 1
                    }
                }
            },
            "2017-01-15": {
                "clicks": 1,
                "impressions": 7,
                "conversions": 0,
                "revenue": 8.26,
                "payout": 2.45,
                "meta": {
                    "device": {
                        "desktop": 4
                    },
                    "os": {
                        "Mac OS": 1
                    },
                    "referer": {
                        "blogslog.in": 4
                    },
                    "country": {
                        "CA": 3,
                        "IN": 5
                    }
                }
            },
            "2017-01-16": {
                "clicks": 1,
                "impressions": 0,
                "conversions": 0,
                "revenue": 0,
                "payout": 0,
                "meta": {
                    "device": {
                        "desktop": 1
                    },
                    "os": {
                        "Mac OS X": 1
                    },
                    "referer": {
                        "facebook.com": 1
                    },
                    "country": {
                        "IN": 1
                    }
                }
            },
            "2017-01-17": {
                "clicks": 0,
                "impressions": 1,
                "conversions": 0,
                "revenue": 1.18,
                "payout": 0.35,
                "meta": {
                    "device": {
                        "mobile": 1
                    },
                    "os": [],
                    "referer": {
                        "blogslog.in": 1
                    },
                    "country": {
                        "US": 1
                    }
                }
            },
            "2017-01-18": {
                "clicks": 0,
                "impressions": 2,
                "conversions": 0,
                "revenue": 2.36,
                "payout": 0.7,
                "meta": {
                    "device": {
                        "mobile": 2,
                        "desktop": 3,
                        "tablet": 1
                    },
                    "os": {
                        "iOS": 2,
                        "Android": 1,
                        "Mac OS X": 1,
                        "Windows 10": 1
                    },
                    "referer": {
                        "test.com": 5,
                        "blogslog.in": 1
                    },
                    "country": {
                        "US": 2
                    }
                }
            }
        },
        "total": {
            "meta": {
                "device": {
                    "mobile": 4,
                    "desktop": 8,
                    "tablet": 1
                },
                "os": {
                    "Mac OS": 1,
                    "Mac OS X": 2,
                    "iOS": 2,
                    "Android": 1,
                    "Windows 10": 1
                },
                "referer": {
                    "blogslog.in": 7,
                    "facebook.com": 1,
                    "test.com": 5
                },
                "country": {
                    "US": 4,
                    "CA": 3,
                    "IN": 6
                }
            },
            "clicks": 2,
            "impressions": 11,
            "conversions": 0,
            "revenue": 12.98,
            "payout": 3.85
        }
    }
}
```



