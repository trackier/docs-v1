# Update Payout

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | /network/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID} |

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
  http://api.trackier.com/network/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID} \
  -H 'Accept: */*' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'Host: restapi.trackier.io' \
  -H 'Postman-Token: 7029f7b5-6318-436d-a451-76fbd095f2c4,d68bd761-0f5b-4f1f-ad90-48e99792eeca' \
  -H 'User-Agent: PostmanRuntime/7.13.0' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'accept-encoding: gzip, deflate' \
  -H 'cache-control: no-cache' \
  -H 'content-length: 150' \
  -H 'cookie: __cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6' \
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

