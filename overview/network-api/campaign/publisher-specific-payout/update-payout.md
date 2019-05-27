# Update Payout

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | /campaign/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID} |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| goal\_id | string | Goal ID | Yes |
| pids | array | List of Publisher Long ID's | Yes |
| crev | integer | Override Default Revenue \(0,1\) | Yes |
| payout | float | Payout | Yes |
| revenue | float | Revenue \(Required if crev is 1\) | Yes |
| coverage | array | List of GEOs | Yes |

### Example Request

```bash
curl -X POST \
  http://api.trackier.com/campaign/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID} \
  -H 'Accept: */*' \
  -H 'Content-Type: application/json' \
  -H 'Host: api.trackier.com' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'content-length: 150' \
  -b '__cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6' \
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
    "message": "Publisher Specific Payout Updated Successfully",
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

