# Affiliate Earning

| HTTP Method | End Point |
| --- | --- |
| GET | /affiliate/earning/{id} |

## Request Parameters

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/affiliates/earning/{id}?start=2016-10-12&end=2016-10-13"
```

| Key | Type | Description | Required |
| --- | --- | --- | --- |
| start | date \(Y-m-d\) | Start date from which the stats should be displayed | No |
| end | date \(Y-m-d\) | End date till which the stats should be displayed | No |

## Response Body

The response data will be present under "data" in "stats" containing date wise statistics showing clicks, conversions, impressions, and their meta data.

The Meta data contains the clicks and differentiate the data based on the **country, os, device, **and **referer. **

The "total" key contains the summation of all the date wise data

```json
{
  "data": {
    "user": {
      "org_id": "string",
      "username": null,
      "name": "test pub",
      "email": "abc@example.com",
      "password": "7c222fb2927d828af22f592134e8932480637c0d",
      "phone": null,
      "country": "IN",
      "currency": "INR",
      "type": "publisher",
      "login": null,
      "_id": "string",
      "live": true,
      "created": "2016-09-21",
      "modified": "2016-10-01",
      "meta": {}
    },
    "stats": {
      "2016-10-12": {
        "meta": {
          "country": {
            "US": 509,
            "SG": 99,
            "IE": 97,
            "AU": 96,
            "BR": 75,
            "JP": 62,
            "TR": 58,
            "FR": 51,
            "MA": 39,
            "TW": 39,
            "rest": 539
          },
          "device": {
            "desktop": 1694
          },
          "os": {
            "Windows XP": 1072,
            "Windows 7": 561,
            "Windows 8": 29,
            "Windows Vista": 24,
            "Windows 8.1": 4,
            "Windows 2000": 3,
            "Windows": 1
          },
          "referer": {
            "m.facebook.com": 1618,
            "Empty": 75
          }
        },
        "clicks": 1694,
        "impressions": 0,
        "conversions": 0,
        "payout": 1694
      },
      "2016-10-13": {
        "meta": {
          "country": {
            "US": 436,
            "IE": 87,
            "AU": 74,
            "SG": 55,
            "JP": 51,
            "BR": 47,
            "FR": 43,
            "TR": 31,
            "PK": 25,
            "TW": 24,
            "rest": 367
          },
          "device": {
            "desktop": 1240
          },
          "os": {
            "Windows XP": 804,
            "Windows 7": 396,
            "Windows 8": 17,
            "Windows Vista": 14,
            "Windows": 5,
            "Windows 2000": 3,
            "Windows NT 4.0": 1
          },
          "referer": {
            "m.facebook.com": 1185,
            "Empty": 55
          }
        },
        "clicks": 1240,
        "impressions": 0,
        "conversions": 0,
        "payout": 1240
      }
    },
    "total": {
      "meta": {
        "country": {
          "rest": 936,
          "US": 945,
          "SG": 154,
          "IE": 184,
          "AU": 170,
          "BR": 122,
          "JP": 113,
          "TR": 89,
          "FR": 94,
          "MA": 39,
          "TW": 63,
          "PK": 25
        },
        "device": {
          "desktop": 2934
        },
        "os": {
          "Windows XP": 1876,
          "Windows 7": 957,
          "Windows 8": 46,
          "Windows Vista": 38,
          "Windows 8.1": 4,
          "Windows 2000": 6,
          "Windows": 6,
          "Windows NT 4.0": 1
        },
        "referer": {
          "m.facebook.com": 2803,
          "Empty": 130
        }
      },
      "clicks": 2934,
      "impressions": 0,
      "conversions": 0,
      "payout": 2934
    }
  }
}
```

