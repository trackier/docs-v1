# Publisher Specific Payout

#### Note: user\_id field is deprecated

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /network/pub-payout/{CampaignID} | Display all campaign payouts |
| GET | /network/pub-payout/{campaignID}/{PublisherID} | Display Publisher Specific Payout |

## Response body

* _**For all campaign specific payouts**_

  ```bash
  GET /network/pub-payout/{CampaignID} HTTP/1.1
  Host: api.vnative.com
  X-Api-Key: {API-KEY}
  cache-control: no-cache
  Postman-Token: eb9d0af0-18a6-470d-aec9-60a51a450189
  ```

```javascript
 {
    "success": true,
    "data": {
        "payouts": [
            {
                "ad_id": "5c5ebfebb6920d307d68c92c",
                "goal_id": null,
                "user_id": "57c6c75934243d930c8b4581", // Deprecated field
                "rate": 2,
                "coverage": [
                    "ALL"
                ],
                "_id": "5c6158e5b6920d73ad30c120"
            },
            {
                "ad_id": "5c5ebfebb6920d307d68c92c",
                "goal_id": null,
                "user_id": "57fce4921d41c83ab1066193", // Deprecated field
                "rate": 23,
                "coverage": 
                    "ALL"
                ],
                "_id": "5c61706eb6920d070141da76"
            }
        ]
    }
}
```

* _**For single publisher payout**_

  ```bash
  GET /network/pub-payout/{CampaignID}/{PublisherID} HTTP/1.1
  Host: https://api.vnative.com
  X-Api-Key: {API-KEY}
  cache-control: no-cache
  Postman-Token: 6178bc09-4cb9-4990-89f5-7fb724b19be8
  ```

```javascript
{
    "success": true,
    "data": {
        "payouts": [
            {
                "ad_id": "5c5ebfebb6920d307d68c92c",
                "goal_id": null,
                "user_id": "57c6c75934243d930c8b4581", // Deprecated field
                "rate": 2,
                "coverage": [
                    "ALL"
                ],
                "_id": "5c6158e5b6920d73ad30c120"
            }
        ]
    }
}
```

