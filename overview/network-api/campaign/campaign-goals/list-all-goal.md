# List all goal

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /goals/{campId} | Display all the goals |
| GET | /goals/{campId}/{goalId} | Display info of a single goals |

## Response body

Revenue is what is charged from advertiser and payout is what is given to the affiliate

* _**For all the goals**_

  ```bash
  curl -X GET \
    https://api.vnative.com/goals/{campaignId} \
    -H 'Content-Type: application/json' \
    -H 'Postman-Token: 7d1accec-6850-4860-908f-482f7766493f' \
    -H 'cache-control: no-cache' \
    -H 'x-api-key: {API-KEY}'
  ```

```javascript
    {
    "success": true,
    "data": {
        "goals": [
            {
                "_id": "{Goal Id}",
                "title": "Register",
                "value": "reg",
                "type": "public",
                "revenue": 10,
                "payout": 2,
                "currency": "USD"
            },
            {
                "_id": "{Goal Id}",
                "title": "Login",
                "value": "log",
                "type": "public",
                "revenue": 8,
                "payout": 2,
                "currency": "USD"
            }
        ]
    }
}
```

* _**For a single goal**_

  ```bash
  curl -X GET \
    https://api.vnative.com/goals/{campaignId}/{goalId} \
    -H 'Content-Type: application/json' \
    -H 'Postman-Token: a042b83d-235b-430a-810e-f9cd1cf1ea9f' \
    -H 'cache-control: no-cache' \
    -H 'x-api-key: {API-KEY}'
  ```

```javascript
    "success": true,
    "data": {
        "goal": {
            "_id": "{Goal Id}",
            "title": "Register",
            "value": "Reg",
            "type": "public",
            "revenue": 10,
            "payout": 2,
            "currency": "USD"
        }
    }
}
```

