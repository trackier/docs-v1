# Stats

| HTTP Method | End Point |
| :--- | :--- |
| GET | /network/stats |

## Request Parameters

| Key | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| start | string | Start Date in YYYY-mm-dd format | yes |
| end | string | End Date in YYYY-mm-dd format | yes |

## Response body

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 0d66f7bd-3e61-7401-4d34-55092afb8f8e" "https://api.trackier.com/network/stats?start=2017-01-01&end=2017-01-18"
```

```javascript
{
    "success": true,
    "data": {
        "stats": {
            "2017-01-01": {
                "meta": {
                    "device": {
                        "desktop": 1
                    },
                    "os": {
                        "Mac OS X": 1
                    },
                    "referer": {
                        "Empty": 1
                    },
                    "country": {
                        "IN": 1
                    }
                },
                "clicks": 1,
                "impressions": 0,
                "conversions": 0,
                "revenue": 0
            },
            "2017-01-02": {
                "meta": {
                    "device": {
                        "desktop": 1
                    },
                    "os": {
                        "Windows 10": 1
                    },
                    "referer": {
                        "Empty": 1
                    },
                    "country": {
                        "IN": 1
                    }
                },
                "clicks": 1,
                "impressions": 0,
                "conversions": 0,
                "payout": 0.01,
                "revenue": 0.15
            },
            "2017-01-03": {
                "meta": {
                    "device": {
                        "desktop": 2
                    },
                    "os": {
                        "Windows 10": 2
                    },
                    "referer": {
                        "Empty": 2
                    },
                    "country": {
                        "IN": 2
                    }
                },
                "clicks": 2,
                "impressions": 0,
                "conversions": 0,
                "payout": 0.001,
                "revenue": 0.006
            },
            "2017-01-04": {
                "meta": {
                    "device": {
                        "desktop": 2
                    },
                    "os": {
                        "Windows 10": 1,
                        "Mac OS X": 1
                    },
                    "referer": {
                        "Empty": 2
                    },
                    "country": {
                        "IN": 2
                    }
                },
                "clicks": 2,
                "impressions": 0,
                "conversions": 0,
                "payout": 0.1,
                "revenue": 10
            },
            "2017-01-05": {
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
                "revenue": 0
            },
            "2017-01-08": {
                "meta": {
                    "device": {
                        "desktop": 3
                    },
                    "os": {
                        "Mac OS X": 3
                    },
                    "referer": {
                        "Empty": 3
                    },
                    "country": {
                        "IN": 3
                    }
                },
                "clicks": 3,
                "impressions": 0,
                "conversions": 0,
                "payout": 1.2,
                "revenue": 1.8
            },
            "2017-01-09": {
                "meta": {
                    "device": {
                        "desktop": 7
                    },
                    "os": {
                        "Mac OS": 3
                    },
                    "referer": {
                        "blogslog.in": 7
                    },
                    "country": {
                        "IN": 6,
                        "US": 3
                    }
                },
                "clicks": 3,
                "impressions": 6,
                "conversions": 0,
                "payout": 2,
                "revenue": 10
            },
            "2017-01-10": {
                "meta": {
                    "device": {
                        "mobile": 11,
                        "desktop": 6
                    },
                    "os": {
                        "Android": 3,
                        "Mac OS X": 2,
                        "Windows 10": 1,
                        "Symbian OS": 1,
                        "Linux": 1,
                        "iOS": 1
                    },
                    "referer": {
                        "Empty": 9,
                        "blogslog.in": 8
                    },
                    "country": {
                        "US": 14,
                        "IN": 4,
                        "XX": 1
                    }
                },
                "clicks": 9,
                "impressions": 10,
                "conversions": 0,
                "payout": 0.1,
                "revenue": 10
            },
            "2017-01-11": {
                "meta": {
                    "device": {
                        "desktop": 5
                    },
                    "os": [],
                    "referer": {
                        "blogslog.in": 5
                    },
                    "country": {
                        "US": 3,
                        "IN": 2
                    }
                },
                "clicks": 0,
                "impressions": 5,
                "conversions": 0,
                "payout": 0,
                "revenue": 0
            },
            "2017-01-12": {
                "meta": {
                    "device": {
                        "mobile": 8,
                        "desktop": 3
                    },
                    "os": [],
                    "referer": {
                        "blogslog.in": 11
                    },
                    "country": {
                        "US": 13
                    }
                },
                "clicks": 0,
                "impressions": 13,
                "conversions": 0,
                "payout": 0,
                "revenue": 0
            },
            "2017-01-13": {
                "meta": {
                    "device": {
                        "desktop": 4,
                        "mobile": 2
                    },
                    "os": {
                        "Android": 2,
                        "Mac OS X": 1
                    },
                    "referer": {
                        "Empty": 3,
                        "blogslog.in": 3
                    },
                    "country": {
                        "US": 4,
                        "IN": 3,
                        "XX": 1
                    }
                },
                "clicks": 3,
                "impressions": 5,
                "conversions": 0,
                "payout": 0,
                "revenue": 0
            },
            "2017-01-14": {
                "meta": {
                    "device": {
                        "mobile": 9,
                        "desktop": 5
                    },
                    "os": {
                        "Mac OS X": 5
                    },
                    "referer": {
                        "blogslog.in": 9,
                        "Empty": 5
                    },
                    "country": {
                        "US": 14,
                        "IN": 5
                    }
                },
                "clicks": 5,
                "impressions": 14,
                "conversions": 0,
                "payout": 0.7,
                "revenue": 2.36
            },
            "2017-01-15": {
                "meta": {
                    "device": {
                        "desktop": 16
                    },
                    "os": {
                        "Mac OS": 8
                    },
                    "referer": {
                        "blogslog.in": 16
                    },
                    "country": {
                        "US": 8,
                        "IN": 7,
                        "CA": 5,
                        "": 2
                    }
                },
                "clicks": 8,
                "impressions": 12,
                "conversions": 2,
                "payout": 3.65,
                "revenue": 9.41
            },
            "2017-01-16": {
                "meta": {
                    "device": {
                        "desktop": 7,
                        "mobile": 6
                    },
                    "os": {
                        "Mac OS X": 1,
                        "Mac OS": 1
                    },
                    "referer": {
                        "blogslog.in": 12,
                        "facebook.com": 1
                    },
                    "country": {
                        "US": 10,
                        "IN": 4
                    }
                },
                "clicks": 2,
                "impressions": 12,
                "conversions": 0,
                "payout": 0,
                "revenue": 0
            },
            "2017-01-17": {
                "meta": {
                    "device": {
                        "desktop": 22,
                        "mobile": 5
                    },
                    "os": {
                        "Mac OS X": 6,
                        "Windows 10": 5,
                        "Linux": 4,
                        "Windows 7": 4,
                        "Windows 8.1": 2,
                        "Ubuntu": 1
                    },
                    "referer": {
                        "facebook.com": 11,
                        "twitter.com": 8,
                        "blogslog.in": 5,
                        "pinterest.com": 2,
                        "Empty": 1
                    },
                    "country": {
                        "CN": 11,
                        "US": 9,
                        "HK": 2,
                        "PK": 1,
                        "ID": 1,
                        "NL": 1,
                        "AZ": 1,
                        "IN": 1
                    }
                },
                "clicks": 22,
                "impressions": 5,
                "conversions": 0,
                "payout": 6.95,
                "revenue": 4.48
            },
            "2017-01-18": {
                "meta": {
                    "device": {
                        "desktop": 4
                    },
                    "os": [],
                    "referer": {
                        "blogslog.in": 4
                    },
                    "country": {
                        "US": 5
                    }
                },
                "clicks": 0,
                "impressions": 5,
                "conversions": 0,
                "payout": 0.7,
                "revenue": 2.36
            }
        },
        "total": {
            "meta": {
                "device": {
                    "desktop": 89,
                    "mobile": 41
                },
                "os": {
                    "Mac OS X": 20,
                    "Windows 10": 10,
                    "Mac OS": 13,
                    "Android": 5,
                    "Symbian OS": 1,
                    "Linux": 5,
                    "iOS": 1,
                    "Windows 7": 4,
                    "Windows 8.1": 2,
                    "Ubuntu": 1
                },
                "referer": {
                    "Empty": 27,
                    "blogslog.in": 81,
                    "facebook.com": 12,
                    "twitter.com": 8,
                    "pinterest.com": 2
                },
                "country": {
                    "IN": 42,
                    "US": 83,
                    "XX": 2,
                    "CA": 5,
                    "": 2,
                    "CN": 11,
                    "HK": 2,
                    "PK": 1,
                    "ID": 1,
                    "NL": 1,
                    "AZ": 1
                }
            },
            "clicks": 62,
            "impressions": 87,
            "conversions": 2,
            "revenue": 50.566,
            "payout": 15.411
        }
    }
}
```

