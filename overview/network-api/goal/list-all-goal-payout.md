# List all goal payout

| **HTTP method** | End Point |
| :--- | :--- |
| GET | /goal/payout/{goalID} |

## **Response body parameters**

* _**Get all goal payout**_

```bash
curl -X GET \
  http://api.vnative.com/goal/payout/5c84f31bdc7138652b371792 \
  -H 'Postman-Token: ce8b6031-721a-4589-be90-c525f4441b16' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "payouts": [
            {
                "_id": "5c84f31bdc7138652b371793",
                "coverage": [
                    "ALL"
                ],
                "revenue": 10,
                "payout": 2,
                "model": "fixed"
            },
            {
                "_id": "5c84f31bdc7138652b371794",
                "coverage": [
                    "US"
                ],
                "revenue": 0.9,
                "payout": 0.3,
                "model": "fixed"
            }
        ]
    }
}
```

