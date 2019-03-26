# **Affiliate Report**

| **HTTP method** | **End Point** | **Description** |
| --- | --- |
| GET | /affiliate/report | Get overall report |

## Get Details

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 52d70764-86fd-a306-8e5c-1af3bd548c1b" "https://api.vnative.com/affiliate/report?start=2016-12-01&end=2016-12-31"
```

### **Response body**

```json
{
    "success": true,
    "data": {
        "links": [
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-10-28",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-11-30",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-12-03",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-12-04",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-12-07",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-12-15",
                "modified": null,
                "meta": []
            },
            {
                "user_id": "string",
                "ad_id": "string",
                "domain": "dobolly.com",
                "_id": "string",
                "live": true,
                "created": "2016-12-17",
                "modified": null,
                "meta": []
            }
        ],
        "performance": [
            {
                "created": "2016-12-27",
                "clicks": 1,
                "conversions": 1,
                "impressions": 0,
                "revenue": 0.1
            },
            {
                "created": "2016-12-23",
                "clicks": 2,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0
            },
            {
                "created": "2016-12-21",
                "clicks": 7,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0
            },
            {
                "created": "2016-12-20",
                "clicks": 1,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.01
            },
            {
                "created": "2016-12-19",
                "clicks": 1,
                "conversions": 1,
                "impressions": 0,
                "revenue": 0.1
            },
            {
                "created": "2016-12-17",
                "clicks": 8,
                "conversions": 6,
                "impressions": 0,
                "revenue": 0.61
            },
            {
                "created": "2016-12-15",
                "clicks": 3,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0
            },
            {
                "created": "2016-12-13",
                "clicks": 1,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.12
            },
            {
                "created": "2016-12-08",
                "clicks": 2,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.24
            },
            {
                "created": "2016-12-07",
                "clicks": 1,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0
            },
            {
                "created": "2016-12-06",
                "clicks": 45,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.45
            },
            {
                "created": "2016-12-04",
                "clicks": 99,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.99
            },
            {
                "created": "2016-12-03",
                "clicks": 4,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.24
            },
            {
                "created": "2016-12-02",
                "clicks": 1,
                "conversions": 0,
                "impressions": 0,
                "revenue": 0.12
            }
        ],
        "start": "2016-12-01",
        "end": "2016-12-31",
        "campaigns": [
            {
                "_id": "string",
                "image": "57fd4c1373708.png",
                "title": "Tetë vjedhje në të njëjtën shtëpi (Video) - Telegrafi",
                "preview_url": "http://www.telegrafi.com/tete-vjedhje-ne-te-njejten-shtepi-video/",
                "category": [
                    "News"
                ],
                "live": false,
                "description": null
            },
            {
                "_id": "string",
                "image": "583e74dda00e4.jpg",
                "title": "Multiplexes reduce popcorn prices, now combo pack of ticket+popcorn at only 2000 Rs",
                "preview_url": "http://www.fakingnews.firstpost.com/entertainment/multiplexes-reduce-popcorn-prices-now-combo-pack-ticketpopcorn-2000-rs-18405",
                "category": [
                    "Politics ",
                    "News"
                ],
                "live": true,
                "description": null
            },
            {
                "_id": "string",
                "image": "57fa5e164ff46.png",
                "title": "Performance Marketing Software",
                "preview_url": "http://vnative.com/signup/",
                "category": [
                    "Technology"
                ],
                "live": false,
                "description": "Get Started with a 30-day free Trial!!!"
            },
            {
                "_id": "string",
                "image": "5831dd17a33b9.jpeg",
                "title": "Gusty Winds Tore Apart India’s Largest Flag In Telangana",
                "preview_url": "http://topyaps.com/countrys-largest-flag-damage",
                "category": [
                    "News"
                ],
                "live": false,
                "description": "Just four days after India’s largest flag was unfurled in Telangana, gusty winds tore it apart. Authorities were forced to take it down."
            },
            {
                "_id": "string",
                "image": "57f88e76df82f.png",
                "title": "SwiftIntern - Android Apps on Google Play",
                "preview_url": "https://play.google.com/store/apps/details?id=com.swiftintern",
                "category": [
                    "Technology"
                ],
                "live": true,
                "description": "No college Students should graduate without any professional experience."
            },
            {
                "_id": "string",
                "image": "5852549669438.jpg",
                "title": "Deep Link Demo - Android Apps on Google Play",
                "preview_url": "https://play.google.com/store/apps/details?id=xyz.abhaychauhan.www.deeplink",
                "category": [
                    "Technology",
                    "Electric products"
                ],
                "live": true,
                "description": "Deep Link Demo App"
            },
            {
                "_id": "string",
                "image": "58551c3062602.png",
                "title": "Traffic Arbitrage Book",
                "preview_url": "http://planyourtours.com/product/traffic-arbitrage-book/",
                "category": [
                    "Technology"
                ],
                "live": true,
                "description": "Get Started with doubling your money"
            }
        ],
        "campaigns_revenue": {
            "campaign_id_1": {
                "clicks": 0
            },
            "campaign_id_2": {
                "clicks": 7,
                "conversions": 0,
                "impressions": 0,
                "payout": 0.07,
                "revenue": 0.124444
            },
            "campaign_id_3": {
                "clicks": 2,
                "conversions": 0,
                "impressions": 0,
                "payout": 0,
                "revenue": 0
            },
            "string": {
                "clicks": 145,
                "conversions": 0,
                "impressions": 0,
                "payout": 1.45,
                "revenue": 2.577779
            },
            "string": {
                "clicks": 2,
                "conversions": 0,
                "impressions": 0,
                "payout": 0,
                "revenue": 0
            },
            "string": {
                "clicks": 17,
                "conversions": 0,
                "impressions": 0,
                "payout": 0,
                "revenue": 0
            },
            "string": {
                "clicks": 4,
                "conversions": 0,
                "impressions": 0,
                "payout": 0,
                "revenue": 0
            }
        }
    }
}
```