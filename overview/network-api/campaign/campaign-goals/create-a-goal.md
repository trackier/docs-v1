# Create a Goal

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/goal** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| goal | object | Goal Basic Information | No |
| payouts | array | Goal Payouts Array | No |

**Goal Object**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title | string | Goal Title | No |
| value | string | Goal Value | No |
| type | string | public/private | No |
| ad\_id | string | Campaign ID | No |
| model | string | fixed/percentage | No |

**Payout Object**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| payout | float | Goal Payout | No |
| revenue | float | Goal Revenue | No |
| coverage | Array | Country Code 2 Letter | No |

### Example Request

```bash
curl -X POST \
  http://api.trackier.com/goal \
  -H 'X-Api-Key: {API_KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "goal": {
        "title": "API GOAL 2",
        "value": "API_GOAL_23",
        "type": "private",
        "ad_id": "5d634a5489d4464591741232",
        "model": "fixed"
    },
    "payouts": [
        {
            "payout":4,
            "revenue":20,
            "coverage": ["IN"]
        },
        {
            "payout":5,
            "revenue":30,
            "coverage": ["US"]
        }
    ]
}'
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
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
        ],
        "message": "Goal Created Successfully!!"
    }
}
```

