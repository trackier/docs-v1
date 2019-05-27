# List Payout

#### Note: user\_id field is deprecated

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /campaign/pub-payout/{CampaignID} | Display all campaign payouts |
| GET | /campaign/pub-payout/{campaignID}/{PublisherID} | Display Publisher Specific Payout |

## Response body

* _**For all campaign specific payouts**_

  ```bash
  GET /campaign/pub-payout/{CampaignID} HTTP/1.1
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
                "ad_id": "5c865f33b6920d5fb344418e",
                "goal_id": "5ce689b2b6920d0a303633f4",
                "user_id": "57c6c75934243d930c8b4581",
                "rate": 8,
                "coverage": [
                    "ALL"
                ],
                "pids": [
                    "57c6c75934243d930c8b4581",
                    "5c6bff16b6920d39975e3712"
                ],
                "crev": 1,
                "_id": "5ce79b42b6920d69cd1cecfc"
            },
            {
                "ad_id": "5c865f33b6920d5fb344418e",
                "goal_id": "5ce68976b6920d0a303633eb",
                "user_id": "5c2dd05fb6920d5a14541cf6",
                "rate": 3,
                "coverage": [
                    "ALL"
                ],
                "pids": [
                    "5c2dd05fb6920d5a14541cf6"
                ],
                "crev": 0,
                "_id": "5ce90034b6920d7c942fa3d6"
            }
        ]
    }
}
```

* _**For single publisher payout**_

  ```bash
  GET /campaign/pub-payout/{CampaignID}/{PublisherID} HTTP/1.1
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
                "ad_id": "5c865f33b6920d5fb344418e",
                "goal_id": "5ce689b2b6920d0a303633f4",
                "user_id": "57c6c75934243d930c8b4581",
                "rate": 8,
                "coverage": [
                    "ALL"
                ],
                "pids": [
                    "57c6c75934243d930c8b4581",
                    "5c6bff16b6920d39975e3712"
                ],
                "crev": 1,
                "_id": "5ce79b42b6920d69cd1cecfc"
            }
        ]
    }
}
```

