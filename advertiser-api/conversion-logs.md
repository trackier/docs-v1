 ## Advertiser Conversion Logs

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | [/advertiser/conversion-logs](/advertiser-api/conversion-logs.md) | Export Conversion Logs |

### **Sample Request**

```php
curl -X GET \
  'http://api.vnative.com/advertiser/conversion-logs?start=2019-01-01&limit=1&page=2' \
  -H 'Postman-Token: 9d508762-47f8-4247-8529-a4f87435a670' \
  -H 'cache-control: no-cache' \
  -H 'x-api-key: {key}' 
```

| Key | Type | Description | Nullable |
| :--- | :---: | :--- | :---: |
| start | String (YYYY-mm-DD) | Conversion Log import start date | Yes |
| end | String (YYYY-mm-DD) | Conversion Log import end date | Yes |
| limit | Integer | How many Logs you want. | Yes |
| page | Integer | Page Number | Yes |
[](/network-ops/conversions.md)
### Sample **Response body**

```json
{
    "success": true,
    "query": {
        "start": "2019-01-01",
        "end": "2019-01-07",
        "fields": [
            "_id",
            "cid",
            "campaign_id",
            "campaign_name",
            "method",
            "ipaddr",
            "created",
            "sub1"
        ]
    },
    "limit": 1,
    "page": 2,
    "columns": {
        "cid": "Click ID",
        "source": "Source",
        "elapsed_time": "Click to Conversion Time",
        "method": "Conversion Method",
        "sale": "Sale Amount",
        "ipaddr": "IP Address",
        "city": "City",
        "isp": "ISP",
        "p1": "P1",
        "p2": "P2",
        "p3": "P3",
        "p4": "P4",
        "p5": "P5",
        "p6": "P6",
        "p7": "P7",
        "p8": "P8",
        "p9": "P9",
        "p10": "P10",
        "sub1": "SUB1",
        "sub2": "SUB2",
        "sub3": "SUB3",
        "sub4": "SUB4",
        "sub5": "SUB5",
        "sub6": "SUB6",
        "sub7": "SUB7",
        "sub8": "SUB8",
        "sub9": "SUB9",
        "sub10": "SUB10",
        "os": "OS",
        "type": "Type",
        "txnId": "Txn ID",
        "urlId": "URL ID",
        "device_id": "Device ID",
        "gaid": "GAID",
        "idfa": "IDFA",
        "app_id": "App ID",
        "app_name": "App Name",
        "aid": "Android ID",
        "cr_name": "Creative Name",
        "sl": "Smart Link",
        "adid": "Campaign",
        "country": "Country",
        "browser": "Browser",
        "device": "Device",
        "_id": "ID",
        "created": "Created",
        "clickIp": "Click IP",
        "advertiser_id": "Advertiser ID",
        "advertiser_long_id": "Advertiser Long ID",
        "advertiser_name": "Advertiser Name",
        "campaign_id": "Campaign ID",
        "campaign_long_id": "Campaign Long ID",
        "campaign_name": "Campaign Name",
        "goal_id": "Goal ID",
        "goal_name": "Goal Title",
        "url_long_id": "URL Long ID",
        "url_title": "URL Title"
    },
    "records": [
        {
            "_id": "5c2f71547379e805dbd40312",
            "cid": "5c2f713c0563850467e3c2da",
            "campaign_id": 16,
            "campaign_name": "Traffic Arbitrage Book",
            "method": "PostBack URL",
            "ipaddr": "196.207.83.0",
            "created": {
                "date": "2019-01-04 20:14:36.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "sub1": null,
            "status": "approved",
            "referer": null
        }
    ],
    "count": 17
}
```



