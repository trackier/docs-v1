# Report

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /advertiser/report | Get overall report |

## Get Details

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: b2cfadc3-0869-22a1-e2ba-467be10bd29e" "https://api.vnative.com/advertiser/report"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "performance": [
            {
                "created": "2016-12-27",
                "clicks": 1,
                "conversions": 1,
                "impressions": 0,
                "debit": 1
            },
            {
                "created": "2016-12-26",
                "clicks": 1,
                "conversions": 1,
                "impressions": 0,
                "debit": 1
            },
            {
                "created": "2016-12-25",
                "clicks": 1,
                "conversions": 0,
                "impressions": 0,
                "debit": 0
            },
            {
                "created": "2016-12-24",
                "clicks": 10,
                "conversions": 4,
                "impressions": 0,
                "debit": 0.75
            },
            {
                "created": "2016-12-23",
                "clicks": 5,
                "conversions": 2,
                "impressions": 0,
                "debit": 0.3
            }
        ],
        "start": "2016-12-23",
        "end": "2016-12-28"
    }
}
```

