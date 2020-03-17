# Custom report

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /network/customReport | Display the customized report |

## Request Parameters

| Key | Value | Description | Required | Default |
| :--- | :--- | :--- | :--- | :--- |
| group\[\] | Any key of groupingMap | Group the data by these values | No | \["adid"\] |
| pid\[\] | Affiliate ID | Display the report only for the selected affiliates | No | All affiliates of the network |
| adid\[\] | Campaign ID | Display the report only for the selected campaigns | No | All Campaigns of publisher |
| start | date in Y-m-d | get record with date greater than this | No | Today |
| end | date in Y-m-d | get record with date less than this | No | Today |

## Response body

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 6eb90347-b96b-207a-3e7b-8f69d2224215" "https://api.trackier.com/network/customReport"
```

```javascript
{
    "success": true,
    "data": {
        "records": [
            {
                "adid": "ALTBalaji – Original_265227824_8590",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Myntra",
                "grossClicks": 459,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "App Campaign (DO NOT EDIT)",
                "grossClicks": 469,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Xtreme NO (DE CPS)",
                "grossClicks": 2,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "NetPincér ételrendel_9136739_1817",
                "grossClicks": 2,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Transaction, Uptime, Load Test",
                "grossClicks": 1401,
                "payout": 1.4,
                "revenue": 2.8,
                "profit": 1.4,
                "approvedConversions": 0
            },
            {
                "adid": "Tiered campaign",
                "grossClicks": 1,
                "payout": 2,
                "revenue": 4,
                "profit": 2,
                "approvedConversions": 1
            },
            {
                "adid": "Traffic Arbitrage Book",
                "grossClicks": 13959,
                "payout": 24.11,
                "revenue": 50.22,
                "profit": 26.11,
                "approvedConversions": 15
            },
            {
                "adid": "Performance Marketing Software",
                "grossClicks": 0,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "[Test] Test campaign",
                "grossClicks": 2,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "boebjdnj",
                "grossClicks": 3,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "jdbvjsadnj",
                "grossClicks": 2,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Demo Gif setting",
                "grossClicks": 1,
                "payout": 0.1,
                "revenue": 0.15,
                "profit": 0.05,
                "approvedConversions": 0
            },
            {
                "adid": "Golden Scent قولدن سنت",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Reverse Mortgage Quiz - CPL",
                "grossClicks": 0,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Test Campaign Don't Change (TARGETING enabled)",
                "grossClicks": 0,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "CPS campaign",
                "grossClicks": 3,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Testing",
                "grossClicks": 6,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Download Your FREE Guide on Traffic Arbitrage NOW! - vNative",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Amazon Shopping",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Sky Bet: Sports Betting on Football &amp; Horse Racing gb_android_com.skybet.app.skybet",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "testing cpi",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "Himank  Sports Services| Best Tennis Coaching in Dubai | Tennis lessons Business Bay Dubai",
                "grossClicks": 1,
                "payout": 0,
                "revenue": 0,
                "profit": 0,
                "approvedConversions": 0
            },
            {
                "adid": "RedMart - Grocery Delivery (Android 4.1+) SG - Non incent",
                "grossClicks": 4,
                "payout": 12.24,
                "revenue": 16.76,
                "profit": 4.53,
                "approvedConversions": 11
            }
        ],
        "total": {
            "grossClicks": 16321,
            "payout": 39.85,
            "revenue": 73.94,
            "profit": 34.09,
            "approvedConversions": 27
        },
        "affs": [
            {
                "_id": "57c6c75934243d930c8b4581",
                "display_id": 2,
                "name": "Pied Piper"
            },
            {
                "_id": "57e262141d41c81f2b04b8d0",
                "display_id": 5,
                "name": "test pub"
            },
            {
                "_id": "57fce4921d41c83ab1066193",
                "display_id": 6,
                "name": "lirigzon"
            },
            {
                "_id": "580a45201d41c82966347b8b",
                "display_id": 7,
                "name": "Faizan Ayubi"
            },
            {
                "_id": "580e55dc1d41c8765c2b5d1b",
                "display_id": 8,
                "name": "Awesome User"
            },
            {
                "_id": "585306ddb6920d048c717594",
                "display_id": 11,
                "name": "Testing Demo Accounts"
            },
            {
                "_id": "5890caadb6920d06eb17a34e",
                "display_id": 12,
                "name": "Ref Affiliate"
            },
            {
                "_id": "58a334e8b6920d4f863bcaa6",
                "display_id": 13,
                "name": "best"
            },
            {
                "_id": "58bfa0cfb6920d76b868165f",
                "display_id": 15,
                "name": "ABC"
            },
            {
                "_id": "58fcf9ecb6920d55810b95c3",
                "display_id": 17,
                "name": "Publisher VPSOrg"
            },
            {
                "_id": "5918b997b6920d1d8e1254a2",
                "display_id": 19,
                "name": "Ayaz"
            },
            {
                "_id": "5968a418b6920d15884c1265",
                "display_id": 22,
                "name": "New"
            },
            {
                "_id": "5980a682b6920d5a4e362550",
                "display_id": 23,
                "name": "Pubs Tests"
            },
            {
                "_id": "598d915689d44662c764cd54",
                "display_id": 26,
                "name": "Abhay"
            },
            {
                "_id": "5999501689d4461d6e7c1972",
                "display_id": 28,
                "name": "Testing111"
            },
            {
                "_id": "59a54a6b89d4465afb339a32",
                "display_id": 31,
                "name": "account"
            },
            {
                "_id": "59c9e41db6920d34b70d1d8e",
                "display_id": 32,
                "name": "Testing"
            },
            {
                "_id": "59dde621b6920d30e91b13a7",
                "display_id": 33,
                "name": "TANUL "
            },
            {
                "_id": "5a30eab6b6920d740c2fe124",
                "display_id": 66,
                "name": "kajok"
            },
            {
                "_id": "5a350ce8b6920d2f2d404def",
                "display_id": 67,
                "name": "new"
            },
            {
                "_id": "5a81e726b6920d49e23c4138",
                "display_id": 910,
                "name": "John Robert"
            },
            {
                "_id": "5a9a1835b6920d1fb46aa16e",
                "display_id": 912,
                "name": "Adhar"
            },
            {
                "_id": "5aa2a9f0b6920d53d259115a",
                "display_id": 917,
                "name": "StephenMooge"
            },
            {
                "_id": "5aa3a348b6920d3deb1da069",
                "display_id": 918,
                "name": "Test Publisher"
            },
            {
                "_id": "5aa3d570b6920d4797762e50",
                "display_id": 919,
                "name": "Demo Test Pub"
            },
            {
                "_id": "5ab0d66bb6920d61a2322d8b",
                "display_id": 920,
                "name": "Facebook"
            },
            {
                "_id": "5ac0b7cdb6920d66ab0ec0ea",
                "display_id": 922,
                "name": "Nishant"
            },
            {
                "_id": "5af54c6fb6920d6cda186352",
                "display_id": 925,
                "name": "VV Pub"
            },
            {
                "_id": "5b0e0942b6920d6cf7413494",
                "display_id": 928,
                "name": "xyz"
            },
            {
                "_id": "5b0e3bdbb6920d0fa353e344",
                "display_id": 929,
                "name": "xyz123"
            },
            {
                "_id": "5b324fe3b6920d1201493d75",
                "display_id": 933,
                "name": "DEMO Publisher"
            },
            {
                "_id": "5b44464ab6920d2152063e97",
                "display_id": 939,
                "name": "Nimish Bansal"
            },
            {
                "_id": "5b483989b6920d7138051c62",
                "display_id": 940,
                "name": "pub11"
            },
            {
                "_id": "5b485f00b6920d06391f70e2",
                "display_id": 942,
                "name": "temppub"
            },
            {
                "_id": "5b48a3fab6920d38007fec6f",
                "display_id": 943,
                "name": "Abhay Chauhan"
            },
            {
                "_id": "5b752710b6920d5f0f60ff98",
                "display_id": 946,
                "name": "abcd"
            },
            {
                "_id": "5b752c7db6920d61f019b822",
                "display_id": 947,
                "name": "abcde"
            },
            {
                "_id": "5b88eec8b6920d71b845f022",
                "display_id": 952,
                "name": "Naruto"
            },
            {
                "_id": "5b88ef51b6920d71b845f027",
                "display_id": 953,
                "name": "hack"
            },
            {
                "_id": "5b90d62db6920d5d4928a427",
                "display_id": 954,
                "name": "Pratiksha Chaudhari"
            },
            {
                "_id": "5b9608c4b6920d08d334533b",
                "display_id": 956,
                "name": "qwer"
            },
            {
                "_id": "5bacac59b6920d54423a831a",
                "display_id": 957,
                "name": "User Abhay"
            },
            {
                "_id": "5bb73f2fb6920d7e5e3e45bf",
                "display_id": 959,
                "name": "Abhay Chauhan - AppAttribution"
            },
            {
                "_id": "5bc81c39b6920d5a4a0db453",
                "display_id": 960,
                "name": "ajax"
            },
            {
                "_id": "5bdafd8289d4461ce101e644",
                "display_id": 961,
                "name": "AFF ABHAY"
            },
            {
                "_id": "5c2b526cb6920d2bd7729da7",
                "display_id": 1216,
                "name": "Abhay Chauha (AT)"
            },
            {
                "_id": "5c2b5a0cb6920d306b1fab3b",
                "display_id": 1217,
                "name": "TP3"
            },
            {
                "_id": "5c2b5a42b6920d306b1fab3f",
                "display_id": 1218,
                "name": "TP4"
            },
            {
                "_id": "5c2b5b02b6920d312d1708db",
                "display_id": 1219,
                "name": "TP5"
            },
            {
                "_id": "5c2b5b26b6920d306b1fab44",
                "display_id": 1220,
                "name": "TP6"
            },
            {
                "_id": "5c2c80f9b6920d774711045c",
                "display_id": 1221,
                "name": "Himanshu Tiwari"
            },
            {
                "_id": "5c2dbe73b6920d4bf724e0c9",
                "display_id": 1222,
                "name": "AdsFlourish"
            },
            {
                "_id": "5c2dd05fb6920d5a14541cf6",
                "display_id": 1223,
                "name": "User Abhay Gmail"
            },
            {
                "_id": "5c330fadb6920d6ecd2ad9e4",
                "display_id": 1224,
                "name": "Test"
            },
            {
                "_id": "5c345309b6920d3db84c7543",
                "display_id": 1225,
                "name": "123"
            }
        ],
        "ads": [],
        "groupingMap": {
            "adid": "Campaign",
            "campaign_id": "Campaign ID",
            "campaign_long_id": "Campaign Long ID",
            "external_offer_id": "External Offer ID",
            "pid": "Publisher",
            "publisher_id": "Publisher ID",
            "publisher_long_id": "Publisher Long ID",
            "source": "Source (Sub Publisher)",
            "aff_manager": "Publisher Manager",
            "advertiser": "Advertiser",
            "advertiser_id": "Advertiser ID",
            "adv_manager": "Advertiser Manager",
            "goalName": "Goal Name",
            "goalId": "Goal ID",
            "sl": "Smart Link",
            "ro": "Referrer Campaign",
            "ro_id": "Referrer Campaign ID",
            "urlTitle": "Landing Page",
            "urlId": "Landing Page ID (URL ID)",
            "device": "Device",
            "os": "Operating System",
            "country": "Country (GEO)",
            "created": "Date",
            "month": "Month"
        },
        "report_currency": "USD",
        "query": {
            "start": "2019-01-01",
            "end": "2019-01-10",
            "group": [
                "adid"
            ],
            "fields": [
                "grossClicks",
                "payout",
                "revenue",
                "profit",
                "approvedConversions"
            ]
        },
        "fieldMap": {
            "uniqueClicks": "Unique Clicks",
            "rejectedClicks": "Rejected Clicks",
            "grossClicks": "Gross Clicks",
            "impressions": "Impressions",
            "campaign_payout": "Campaign Payout",
            "campaign_revenue": "Campaign Revenue",
            "payout": "Payout",
            "revenue": "Revenue",
            "profit": "Profit",
            "epc": "Earning Per Click (EPC)",
            "ctr": "Click Through Rate (CTR)",
            "cr": "Conversion Rate (CR)",
            "saleAmount": "Sale Amount",
            "pendingTotalConversions": "Pending Conversions",
            "cancelledConversions": "Cancelled Conversions",
            "rejectedConversions": "Rejected Conversions",
            "grossConversions": "Gross Conversions",
            "grossRevenue": "Gross Revenue",
            "pendingSaleAmount": "Pending Sale Amount",
            "pendingPayout": "Pending Payout",
            "pendingRevenue": "Pending Revenue",
            "elapsedRange1": "Conversions (< 2 min)",
            "elapsedRange2": "Conversions (2-10 min)",
            "elapsedRange3": "Conversions (10-30 min)",
            "elapsedRange4": "Conversions (0.5-5 hr)",
            "elapsedRange5": "Conversions (> 5 hr)",
            "approvedConversions": "Approved Conversions"
        }
    }
}
```

