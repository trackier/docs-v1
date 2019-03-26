# Add a goal payout

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /goal/payout/{goalID} |

## **Request body parameters**

```bash
curl -X POST \
  http://api.vnative.com/goal/payout/5c84f31bdc7138652b371792 \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: b612ea51-c51c-4713-8f75-7a1771f63902' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "payout": 0.6,
    "revenue": 0.7,
    "coverage": ["AU"]
}'
```

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| payout | float | Rate of payout | No |
| revenue | float | Revenue of payout | No |
| coverage | array | Country code | No |

## **Response body parameters**

```javascript
{
    "success": true,
    "payouts": [
        {
            "_id": "5c84f7ebdc7138652c44fad4",
            "coverage": [
                "AU"
            ],
            "revenue": 0.7,
            "payout": 0.6,
            "model": "fixed"
        }
    ]
}
```

