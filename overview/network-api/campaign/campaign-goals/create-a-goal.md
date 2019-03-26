# Create a Goal

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/goals/{campaignId}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title | string | Goal Type -&gt; public, private | No |
| value | string |  | No |
| payout | float |  | No |
| revenue | float |  | No |
| type | string | Goal Type -&gt; public or private | No |

### Example Request

```bash
curl -X POST \
  https://api.vnative.com/goals/{CampaignId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: e1b6affb-13b2-43a8-8528-042db834204d' \
  -H 'cache-control: no-cache' \
  -H 'x-api-key: {API-KEY}' \
  -d '{
    "type": "public",
    "payout":2,
    "revenue": 10,
    "title":"Testing Goal",
    "value": "testing"
}'
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "goal": {
            "_id": "{Goal ID}",
            "title": "Testing Goal",
            "value": "testing",
            "type": "public",
            "revenue": 10,
            "payout": 2,
            "currency": "USD"
        },
        "message": "Goal Saved Successfully!!"
    }
}
```

