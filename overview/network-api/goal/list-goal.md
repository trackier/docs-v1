# List Goal

| **HTTP method** | End Point |
| :--- | :--- |
| GET | /goal |
| GET | /goal/{goalID} |
| GET | /goal/ad/{adId} |

## **Response body parameters**

* _**Get the goal**_

```bash
curl -X GET \
  'http://api.vnative.com/goal?page=1&limit=5' \
  -H 'Postman-Token: af1586f9-da70-4eff-8fe7-79f63c9517d8' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "goals": [
            {
                "_id": "58b2cb37b6920d2e38702b46",
                "title": "Test goal #1",
                "value": null,
                "type": "private"
            },
            {
                "_id": "58b699acb6920d2e38702b63",
                "title": "Testing Goal #1",
                "value": "registration",
                "type": "public"
            },
            {
                "_id": "58cbe9aab6920d71690a3a7b",
                "title": "Testing goal 1",
                "value": null,
                "type": "public"
            },
            {
                "_id": "58d1f47cb6920d39a96f06ca",
                "title": "CPC",
                "value": null,
                "type": "public"
            },
            {
                "_id": "58d3d4c8b6920d38785e19e3",
                "title": "Cart",
                "value": null,
                "type": "public"
            }
        ]
    },
    "pagination": {
        "page": 1,
        "limit": 5,
        "total": 170
    }
}
```

* _**Get a goal info**_

```bash
curl -X GET \
  http://api.vnative.com/goal/5c84a6b5dc7138652c44fad2 \
  -H 'Postman-Token: 12bf0399-95c8-4582-83d3-3525518c7cda' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
    "success": true,
    "data": {
        "goal": {
            "_id": "5c84a6b5dc7138652c44fad2",
            "title": "Api Test Goal Update",
            "value": "200",
            "type": "public"
        },
        "payouts": [
            {
                "_id": "5c84a6b5dc7138652c44fad3",
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

* _**Get campaign wise goal**_

```bash
curl -X GET \
  http://api.vnative.com/goal/ad/5c6417c8b6920d371a1d989e \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 5fbdb3e0-4a8c-4bb9-a4c6-f719151b3838' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "goals": [
            {
                "_id": "5c84fde2dc7138652c44fad5",
                "title": "Api Test Goal",
                "value": "api_test",
                "type": "public"
            }
        ]
    },
    "pagination": {
        "page": 1,
        "limit": 50,
        "total": 1
    }
}
```

