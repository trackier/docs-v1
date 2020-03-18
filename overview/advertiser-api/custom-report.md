# Custom Report

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /advertiser/customReport | Display the Custom Report for the advertiser |

## Request Parameters

| Key | Value | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| group\[\] | Any key of groupingMap | Group the data by these values | No | \["adid"\] |
| adid\[\] | Campaign ID | Display the report only for the selected campaigns | No | All Campaigns of publisher |
| start | date in Y-m-d | get record with date greater than this | No | Today |
| end | date in Y-m-d | get record with date less than this | No | Today |

## Response body

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 2a90e180-ad2b-3a79-f40e-f4c9b83c2b0e" "https://api.trackier.com/advertiser/customReport?group[]=device&group[]=adid"
```

```javascript
{
    "success": true,
    "data": {
        "ads": [

        ],
        "records": [
            {
                "clicks": 2,
                "revenue": 19.8,
                "Campaign": "Demo Gif setting ",
                "Device": "desktop"
            },
            {
                "impressions": 3,
                "revenue": 0,
                "Campaign": "Demo Gif setting ",
                "Device": "mobile"
            },
            {
                "impressions": 3,
                "revenue": 0,
                "Campaign": "Tracking Image – Plan Your Tours",
                "Device": "mobile"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "vNative Publisher - Android Apps on Google Play",
                "Device": "desktop"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "UEFA Champions League Top Goal Scorers of All-Times – blogslog",
                "Device": "desktop"
            },
            {
                "impressions": 4,
                "revenue": 0,
                "Campaign": "Performance Marketing Software",
                "Device": "mobile"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "Zbardhet skema/ Si i grabiste milionat e bankave grupi i ",
                "Device": "desktop"
            },
            {
                "impressions": 4,
                "revenue": 0,
                "Campaign": "SwiftIntern - Android Apps on Google Play",
                "Device": "mobile"
            },
            {
                "impressions": 3,
                "revenue": 0,
                "Campaign": "Air India's Ranking In The World's Worst Airlines Is Pretty Accurate",
                "Device": "mobile"
            },
            {
                "impressions": 2,
                "revenue": 0,
                "Campaign": "DailyObjects The Ocean Tote Bag | Skoov",
                "Device": "desktop"
            },
            {
                "impressions": 5,
                "revenue": 0,
                "Campaign": "Traffic Arbitrage Book",
                "Device": "mobile"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "SwiftIntern - Android Apps on Google Play",
                "Device": "desktop"
            },
            {
                "impressions": 2,
                "revenue": 0,
                "Campaign": "UEFA Champions League Top Goal Scorers of All-Times – blogslog",
                "Device": "mobile"
            },
            {
                "impressions": 2,
                "revenue": 0,
                "Campaign": "Zbardhet skema/ Si i grabiste milionat e bankave grupi i ",
                "Device": "mobile"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "Let's Barter - Android Apps on Google Play (CPI)",
                "Device": "desktop"
            },
            {
                "impressions": 2,
                "revenue": 0,
                "Campaign": "Let's Barter - Android Apps on Google Play (CPI)",
                "Device": "mobile"
            },
            {
                "impressions": 2,
                "revenue": 0,
                "Campaign": "Traffic Arbitrage – Plan Your Tours",
                "Device": "desktop"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "Traffic Arbitrage – Plan Your Tours",
                "Device": "mobile"
            },
            {
                "impressions": 5,
                "revenue": 0,
                "Campaign": "Let's Barter - Android Apps on Google Play (CPA)",
                "Device": "mobile"
            },
            {
                "impressions": 3,
                "revenue": 0,
                "Campaign": "Scientists Claim It Is Possible To Live Forever. | Threezly",
                "Device": "mobile"
            },
            {
                "impressions": 1,
                "revenue": 0,
                "Campaign": "Scientists Claim It Is Possible To Live Forever. | Threezly",
                "Device": "desktop"
            }
        ],
        "groupingMap": {
            "adid": "Campaign",
            "device": "Device",
            "goalId": "Goal",
            "urlId": "Additional URL",
            "os": "Operating System",
            "country": "Country",
            "browser": "Browser"
        },
        "total": {
            "clicks": 2,
            "revenue": 19.8,
            "impressions": 47
        },
        "query": {
            "start": "2017-04-01",
            "end": "2017-04-04",
            "group": [
                "device",
                "adid"
            ],
            "fields": [
                "clicks",
                "impressions",
                "conversions",
                "sales",
                "goals",
                "revenue"
            ]
        }
    }
}
```

