# Custom Report

| HTTP Method | End Point | Description |
| --- | --- | --- |
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
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 2a90e180-ad2b-3a79-f40e-f4c9b83c2b0e" "https://api.vnative.com/affiliate/customReport?start=2017-04-01"
```

```json
{
    "success": true,
    "data": {
        "ads": [

        ],
        "records": [
            {
                "clicks": 2,
                "payout": 0,
                "Campaign": "SwiftIntern - Android Apps on Google Play",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 16,
                "conversions": 1,
                "goals": 2,
                "payout": 593.267,
                "Campaign": "Let's Barter - Android Apps on Google Play (CPA)",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 2,
                "goals": 1,
                "payout": 396,
                "Campaign": "DailyObjects The Ocean Tote Bag | Skoov",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 1,
                "payout": 0,
                "Campaign": "Performance Marketing Software",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 4,
                "conversions": 2,
                "payout": 66,
                "Campaign": "Traffic Arbitrage Book",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 5,
                "sales": 1,
                "payout": 66,
                "Campaign": "Traffic Arbitrage – Plan Your Tours",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 22,
                "payout": 435.6,
                "Campaign": "UEFA Champions League Top Goal Scorers of All-Times – blogslog",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 7,
                "payout": 138.6,
                "Campaign": "Zbardhet skema/ Si i grabiste milionat e bankave grupi i ",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 1,
                "payout": 19.8,
                "Campaign": "Air India's Ranking In The World's Worst Airlines Is Pretty Accurate",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 2,
                "conversions": 1,
                "payout": 6.6,
                "Campaign": "Let's Barter - Android Apps on Google Play (CPI)",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 7,
                "sales": 2,
                "goals": 3,
                "payout": 594,
                "Campaign": "Tracking Image – Plan Your Tours",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 2,
                "payout": 0,
                "Campaign": "Sony HD-SL1 Ultra-Slim Lightweight 1TB External Hard Drive with Backup Manager (Silver) - Buy Sony HD-SL1 Ultra-Slim Lightweight 1TB External Hard Drive with Backup Manager (Silver) Online at Low Price in India - Amazon.in",
                "Publisher": "Publisher Demo"
            },
            {
                "clicks": 6,
                "payout": 0,
                "Campaign": "Scientists Claim It Is Possible To Live Forever. | Threezly",
                "Publisher": "Publisher Demo"
            }
        ],
        "groupingMap": {
            "adid": "Campaign",
            "pid": "Publisher",
            "device": "Device",
            "goalId": "Goal",
            "urlId": "Additional URL",
            "os": "Operating System",
            "country": "Country",
            "browser": "Browser"
        },
        "total": {
            "clicks": 77,
            "payout": "2.32K",
            "conversions": 4,
            "goals": 6,
            "sales": 3
        },
        "query": {
            "start": "2017-04-01",
            "end": "2017-04-04",
            "group": [
                "adid",
                "pid"
            ],
            "pid": [
                "string"
            ],
            "fields": [
                "clicks",
                "impressions",
                "conversions",
                "sales",
                "goals",
                "payout"
            ]
        }
    }
}
```



