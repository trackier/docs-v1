# Custom Report

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /affiliate/customReport | Display the Custom Report for the affiliate |

## Request Parameters

| Key | Value | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| group\[\] | Any key of groupingMap | Group the data by these values | No | \["adid"\] |
| adid\[\] | Campaign ID | Display the report only for the selected campaigns | No | All Campaigns of publisher |
| start | date in Y-m-d | get record with date greater than this | No | Today |
| end | date in Y-m-d | get record with date less than this | No | Today |

## Response body

```bash
curl -X GET 
    -H "X-Api-Key: {key}" 
    -H "Cache-Control: no-cache" 
    -H "Postman-Token: 2a90e180-ad2b-3a79-f40e-f4c9b83c2b0e" 
    "https://api.trackier.com/affiliate/customReport?start=2019-01-01"
```

```javascript
{
    "success": true,
    "data": {
        "records": [
            {
                "adid": "Order food online from India's best food delivery service. Order from restaurants near you",
                "grossClicks": 1,
                "totalConversions": 0,
                "payout": 0
            }
        ],
        "total": {
            "grossClicks": 1,
            "totalConversions": 0,
            "payout": 0
        },
        "ads": [],
        "groupingMap": {
            "adid": "Campaign",
            "campaign_id": "Campaign ID",
            "campaign_long_id": "Campaign Long ID",
            "objective": "Objective",
            "pid": "Publisher",
            "publisher_id": "Publisher ID",
            "publisher_long_id": "Publisher Long ID",
            "source": "Source (Sub Publisher)",
            "goalName": "Goal Name",
            "goalId": "Goal ID",
            "sl": "Smart Link",
            "urlTitle": "Landing Page",
            "urlId": "Landing Page ID (URL ID)",
            "device": "Device",
            "os": "Operating System",
            "country": "Country (GEO)",
            "created": "Date",
            "month": "Month"
        },
        "query": {
            "start": "2019-01-01",
            "end": "2019-03-26",
            "group": [
                "adid"
            ],
            "pid": [
                "5c99cf26b6920d7b2f5e0e05"
            ],
            "fields": [
                "grossClicks",
                "totalConversions",
                "payout"
            ]
        },
        "report_currency": "USD",
        "fieldMap": {
            "uniqueClicks": "Unique Clicks",
            "grossClicks": "Gross Clicks",
            "impressions": "Impressions",
            "payout": "Payout",
            "totalConversions": "Conversions",
            "epc": "Earning Per Click (EPC)",
            "ctr": "Click Through Rate (CTR)",
            "cr": "Conversion Rate (CR)"
        }
    }
}
```

