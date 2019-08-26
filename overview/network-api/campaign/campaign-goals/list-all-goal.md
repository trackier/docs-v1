# List all goal

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /goal/campaign/{campaign\_id} | Display all the goals |
| GET | /goal/{goal\_id} | Display info of a single goals |

## Response body

Revenue is what is charged from advertiser and payout is what is given to the affiliate

* _**For all the goals**_

  ```bash
  curl -X GET \
    https://api.trackier.com/goal/campaign/{campaign_id} \
    -H 'X-Api-Key: {API_KEY}' \
    -H 'cache-control: no-cache'
  ```

```javascript
{
    "success": true,
    "currency": "USD",
    "goals": [
        {
            "goal": {
                "_id": "5d638445b6920d0947195996",
                "title": "API Goal",
                "value": "API_GOAL",
                "type": "private"
            },
            "payouts": [
                {
                    "_id": "5d638445b6920d0947195997",
                    "coverage": [
                        "ALL"
                    ],
                    "revenue": 1000,
                    "payout": 200,
                    "model": "percentage"
                }
            ]
        },
        {
            "goal": {
                "_id": "5d63b89789d44630e06ce792",
                "title": "API GOAL 2",
                "value": "API_GOAL_23",
                "type": "private"
            },
            "payouts": [
                {
                    "_id": "5d63b89789d44630e06ce793",
                    "coverage": [
                        "IN"
                    ],
                    "revenue": 20,
                    "payout": 4,
                    "model": "fixed"
                },
                {
                    "_id": "5d63b89789d44630e06ce794",
                    "coverage": [
                        "US"
                    ],
                    "revenue": 30,
                    "payout": 5,
                    "model": "fixed"
                }
            ]
        }
    ]
}
```

* _**For a single goal**_

  ```bash
  curl -X GET \
    https://api.trackier.com/goal/{goal_id} \
    -H 'X-Api-Key: 580515b376832580515b376887580515b3768dd' \
    -H 'cache-control: no-cache'
  ```

```javascript
   {
    "success": true,
    "data": {
        "goal": {
            "_id": "5d638445b6920d0947195996",
            "title": "API Goal",
            "value": "API_GOAL",
            "type": "private"
        },
        "payouts": [
            {
                "_id": "5d638445b6920d0947195997",
                "coverage": [
                    "ALL"
                ],
                "revenue": 10,
                "payout": 2,
                "model": "fixed"
            }
        ]
    }
}
```

