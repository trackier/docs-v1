# Conversion Logs

| HTTP Method | End Point |
| :--- | :--- |
| GET | /network/conversions |

## Request Parameters

| Key | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| start | string | Start Date in YYYY-MM-DD format | yes |
| end | string | End Date in YYYY-MM-DD format | yes |
| adid | array | Array of campaign Ids | yes |
| pid | array | Array of affiliate Ids | yes |
| fields | array | fields that are to be displayed | yes |
| query | array | variables that are required to be queried | yes |
| cid | string | Value of click id | yes |
| \_id | string | Value of conversion id | yes |

Suppose you want to filter the conversions based on **sub2**

then the corresponding get query would be

```text
?query[]=sub2&sub2=some_value
?query[]=sub1&sub1=some_value_for_sub1    # Every param which is needed for filtering should be sent in query
?query[]=adid&query[]=p1&adid[]=someId&p1=some_p1_val
```

_Remember whatever params you send in query will be visible under the **response.query** object_

## Response body

```bash
curl -H 'X-Api-Key: {key}' -X GET 'https://api.vnative.com/network/conversions?query[]=fields&fields[]=cid&fields[]=method&fields[]=sale&fields[]=ipaddr&fields[]=city&fields[]=isp&fields[]=advertiser_id&fields[]=advertiser_long_id&fields[]=advertiser_name&fields[]=publisher_id&fields[]=publisher_long_id&fields[]=publisher_name&fields[]=pid&fields[]=adid&fields[]=goal_id&fields[]=goal_name&fields[]=campaign_id&fields[]=campaign_long_id&fields[]=campaign_name&fields[]=created'
```

```javascript
{
    "success": true,
    "query": {
        "fields": [
            "source",
            "cid",
            "method",
            "isp",
            "revenue",
            "app_name",
            "payout",
            "status",
            "clickIp"
        ]
    },
    "limit": 500,
    "page": 1,
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
        "note": "Note",
        "payout": "Payout",
        "revenue": "Revenue",
        "ro": "Referrer Campaign",
        "gaid": "GAID",
        "idfa": "IDFA",
        "app_id": "App ID",
        "app_name": "App Name",
        "aid": "Android ID",
        "cr_name": "Creative Name",
        "sl": "Smart Link",
        "adid": "Campaign",
        "pid": "Publisher",
        "country": "Country (GEO)",
        "browser": "Browser",
        "device": "Device",
        "_id": "ID",
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
    "records": {
        "5ce555bbeaee790674925370": {
            "source": "{aff_id}",
            "cid": "5ce555a1e2d9bf048a3cd67b",
            "method": "PostBack URL",
            "isp": "Shyam Spectra Pvt",
            "revenue": 0,
            "app_name": null,
            "payout": 0,
            "status": "approved",
            "clickIp": "180.151.244.0",
            "referer": null
        },
        "5ce28f7bea60a86e65fc4573": {
            "source": "pingdom",
            "cid": "5ce2658fbe6d580479ec52ce",
            "method": "PostBack URL",
            "isp": "Host Europe GmbH",
            "revenue": 0.030303,
            "app_name": null,
            "payout": 0.0151515,
            "status": "cancelled",
            "clickIp": "85.93.93.0",
            "referer": null
        },
        "5ce28f5bc80b5e6db79bcee7": {
            "source": "pingdom",
            "cid": "5ce2658fbe6d580479ec52ce",
            "method": "PostBack URL",
            "isp": "Host Europe GmbH",
            "revenue": 0.030303,
            "app_name": null,
            "payout": 0.0151515,
            "status": "approved",
            "clickIp": "85.93.93.0",
            "referer": null
        }
    },
    "count": 3
}
```

