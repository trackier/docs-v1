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
    "success": true,
    "query": {
        "fields": [
            "cid",
            "method",
            "sale",
            "ipaddr",
            "city",
            "isp",
            "advertiser_id",
            "advertiser_long_id",
            "advertiser_name",
            "publisher_id",
            "publisher_long_id",
            "publisher_name",
            "pid",
            "adid",
            "goal_id",
            "goal_name",
            "campaign_id",
            "campaign_long_id",
            "campaign_name",
            "created",
            "url_long_id",
            "url_title"
        ]
    },
    "limit": 100,
    "page": 1,
    "columns": {
        "cid": "Click ID",
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
        "deviceId": "Mobile SDK Device ID",
        "note": "Note",
        "adid": "Campaign Name",
        "pid": "Publisher Name",
        "country": "Country",
        "browser": "Browser",
        "device": "Device",
        "_id": "ID",
        "created": "Created",
        "clickIp": "Click IP",
        "isBot": "Bot Click",
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
        "url_long_id":"URL Long ID",
        "url_title": "URL Title" 
    },
    "records": {
        "5b3b09fce32f790609c537c2": {
            "cid": "5b3b09f55c1d2d0597f30f16",
            "method": "PostBack URL",
            "sale": 0,
            "ipaddr": "203.92.32.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 923,
            "advertiser_long_id": "5acc962eb6920d7caa65396a",
            "advertiser_name": "App Attribution",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "News App (App attribution)",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 120,
            "campaign_long_id": "5acc966db6920d7caa65396f",
            "campaign_name": "News App (App attribution)",
            "created": {
                "date": "2018-07-03 11:00:36.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "approved",
            "referer": null
        },
        "5b3b0018df7b002088d3e8d5": {
            "cid": "5af5328f5d858006326dcae3",
            "method": "PostBack URL",
            "sale": 0,
            "ipaddr": "47.9.62.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 31,
            "publisher_long_id": "59a54a6b89d4465afb339a32",
            "publisher_name": "vNative Account",
            "pid": "vNative Account",
            "adid": "Test Campaign Don't Change (TARGETING enabled)",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 95,
            "campaign_long_id": "59f5e54cb6920d5b8a343c29",
            "campaign_name": "Test Campaign Don't Change (TARGETING enabled)",
            "created": {
                "date": "2018-07-03 10:18:24.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "cancelled",
            "referer": null
        },
        "5b3afffd83cc7236588f67e2": {
            "cid": "5b3afef38cbcc0059d04506a",
            "method": "PostBack URL",
            "sale": 2,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "Traffic Arbitrage Book (Copy)",
            "goal_id": "5a034eb1b6920d65845d524b",
            "goal_name": "Registration",
            "campaign_id": 97,
            "campaign_long_id": "59fdee4ab6920d4f06278878",
            "campaign_name": "Traffic Arbitrage Book (Copy)",
            "created": {
                "date": "2018-07-03 10:17:57.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "cancelled",
            "referer": null
        },
        "5b3aff2b83cc7236588f67df": {
            "cid": "5b3afef38cbcc0059d04506a",
            "method": "PostBack URL",
            "sale": 2,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "Traffic Arbitrage Book (Copy)",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 97,
            "campaign_long_id": "59fdee4ab6920d4f06278878",
            "campaign_name": "Traffic Arbitrage Book (Copy)",
            "created": {
                "date": "2018-07-03 10:14:27.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "cancelled",
            "referer": null
        },
        "5b3aff2383cc7236588f67dc": {
            "cid": "5b3afef38cbcc0059d04506a",
            "method": "PostBack URL",
            "sale": 1,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "Traffic Arbitrage Book (Copy)",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 97,
            "campaign_long_id": "59fdee4ab6920d4f06278878",
            "campaign_name": "Traffic Arbitrage Book (Copy)",
            "created": {
                "date": "2018-07-03 10:14:19.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "approved",
            "referer": null
        },
        "5b3afe6e83cc7236588f67d9": {
            "cid": "5b3afdf87754e0056b86095f",
            "method": "PostBack URL",
            "sale": 1,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "testing currency",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 193,
            "campaign_long_id": "5b39fbcbb6920d01ce4c2428",
            "campaign_name": "testing currency",
            "created": {
                "date": "2018-07-03 10:11:18.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "approved",
            "referer": null
        },
        "5b3afe5a83cc7236588f67d6": {
            "cid": "5b3afdf87754e0056b86095f",
            "method": "PostBack URL",
            "sale": 0.0152,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "testing currency",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 193,
            "campaign_long_id": "5b39fbcbb6920d01ce4c2428",
            "campaign_name": "testing currency",
            "created": {
                "date": "2018-07-03 10:10:58.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "approved",
            "referer": null
        },
        "5b3afe3883cc7236588f67d3": {
            "cid": "5b3afdf87754e0056b86095f",
            "method": "PostBack URL",
            "sale": 0.1818,
            "ipaddr": "47.31.6.0",
            "city": "New Delhi",
            "isp": "Shyam Spectra Pvt",
            "advertiser_id": 3,
            "advertiser_long_id": "57c4738434243dc57d8b456d",
            "advertiser_name": "Demo",
            "publisher_id": 2,
            "publisher_long_id": "57c6c75934243d930c8b4581",
            "publisher_name": "Pied piper",
            "pid": "Pied Piper",
            "adid": "testing currency",
            "goal_id": null,
            "goal_name": null,
            "campaign_id": 193,
            "campaign_long_id": "5b39fbcbb6920d01ce4c2428",
            "campaign_name": "testing currency",
            "created": {
                "date": "2018-07-03 10:10:24.000000",
                "timezone_type": 3,
                "timezone": "Asia/Kolkata"
            },
            "status": "approved",
            "referer": null
        }
    },
    "count": 8
}
```

