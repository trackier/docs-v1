# Update Goal Payout

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/goal/payout/{goal\_id}/{payout\_id}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| payout | float | Goal Payout | No |
| revenue | float | Goal Revenue | No |
| coverage | Array | Country Code 2 Letter | No |

### Example Request

```bash
curl -X POST \
  https://api.trackier.com/goal/payout/{goal_id}/{payout_id} \
  -H 'X-Api-Key: {API_KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "payout": 10,
    "revenue": 400,
    "coverage": ["US"]
}'
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "payout": [
            {
                "_id": "5d63ccf489d446467f48b0e2",
                "coverage": [
                    "US"
                ],
                "revenue": 400,
                "payout": 10,
                "model": "fixed"
            }
        ],
        "message": "Payout Updated Successfully!!"
    }
}
```

