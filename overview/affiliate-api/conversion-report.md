# Conversion Report

| HTTP Method | End Point |
| :--- | :--- |
| GET | /affiliate/conversions |

## Request Parameters

| Key | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| start | string | Start Date in YYYY-MM-DD format | yes |
| end | string | End Date in YYYY-MM-DD format | yes |
| adid | array | Array of campaign Ids | yes |
| fields | array | fields that are to be displayed | yes |
| cid | string | Value of click id | yes |
| \_id | string | Value of conversion id | yes |

## Response body

```bash
curl -X GET \
  'https://api.trackier.com/affiliate/conversions?start=2019-06-16&end=2019-07-22&_id[]=5d10a98aebde160a0018aa5a&fields[]=sub1,sub2' \
  -H 'Host: api.trackier.com' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "query": {
        "cid": [],
        "_id": [
            "5d10a98aebde160a0018aa5a"
        ],
        "start": "2019-06-16",
        "end": "2019-07-22",
        "fields": [
            "sub1",
            "sub2"
        ]
    },
    "limit": 200,
    "page": 1,
    "columns": {
        "_id": "Conversion ID",
        "cid": "Click ID",
        "source": "Source",
        "elapsed_time": "Click to Conversion Time",
        "method": "Conversion Method",
        "sale": "Sale Amount",
        "ipaddr": "Conversion IP",
        "click_ip": "Click IP",
        "city": "City",
        "region": "Region",
        "isp": "Carrier (ISP)",
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
        "os": "Operating System (OS)",
        "type": "Type",
        "goalId": "Goal ID",
        "txnId": "Txn ID",
        "urlId": "Landing Page",
        "device_id": "Device ID",
        "note": "Note",
        "referer": "Image Pixel Referer",
        "cref": "Click Referer",
        "payout": "Payout",
        "revenue": "Revenue",
        "gaid": "GAID",
        "idfa": "IDFA",
        "app_id": "App ID",
        "app_name": "App Name",
        "aid": "Android ID",
        "cr_name": "Creative Name",
        "sl": "Smart Link",
        "brand": "Device Brand",
        "conn": "Connection Type",
        "click_ua": "Click User Agent",
        "lat": "Latitude",
        "long": "Longitude",
        "adid": "Campaign",
        "pid": "Publisher",
        "country": "Country (GEO)",
        "browser": "Browser",
        "device": "Device",
        "created": "Created",
        "status": "Status",
        "clickIp": "Click IP",
        "advertiser_id": "Advertiser ID",
        "advertiser_long_id": "Advertiser Long ID",
        "advertiser_name": "Advertiser Name",
        "publisher_id": "Publisher ID",
        "publisher_long_id": "Publisher Long ID",
        "publisher_name": "Publisher Name",
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
            "sub1": null,
            "sub2": null,
            "status": "approved",
            "referer": null,
            "method": "Image Pixel"
        }
    ],
    "count": 1
}
```

