# Create Payout

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | /campaign/pub-payout/{CAMPAIGN-ID} |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| goal\_id | string | Goal ID | No |
| pids | array | List of Publisher Long ID's | No |
| crev | integer | Override Default Revenue \(0,1\) | No |
| payout | float | Payout | No |
| revenue | float | Revenue \(Required if crev is 1\) | Yes |
| coverage | array | List of GEOs | Yes |

### Example Request

```bash
curl -X POST \
  http://api.trackier.com/campaign/pub-payout/{CAMPAIGN-ID} \
  -H 'Accept: */*' \
  -H 'Content-Type: application/json' \
  -H 'Host: api.trackier.com' \
  -H 'X-Api-Key: {API-KEY}' \
  -d '{
    "goal_id": "5ce689b2b6920d0a303633f4",
    "pids": ["57c6c75934243d930c8b4581"],
    "crev": 1,
    "revenue": 20,
    "payout": 2,
    "coverage": ["US", "IN"]
}'
```

### **Response body**

```javascript
{
    "success": true,
    "message": "Publisher Specific Payout Created Successfully",
    "data": {
        "payouts": [
            {
                "ad_id": "5c865f33b6920d5fb344418e",
                "goal_id": "5ce689b2b6920d0a303633f4",
                "user_id": "57c6c75934243d930c8b4581",
                "rate": 2,
                "coverage": [
                    "US",
                    "IN"
                ],
                "pids": [
                    "57c6c75934243d930c8b4581"
                ],
                "crev": 1,
                "_id": "5ce9234adc713827912df235"
            }
        ]
    }
}
```

