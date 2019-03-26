## Update** an existing goal payout**

| **HTTP method** | **EndPoint** |
| --- | --- |
| POST | /goal/payout/{goalId}/{payoutID} |

### **Request body parameters**

```bash
curl -X POST \
  http://api.vnative.com/goal/payout/5c84f31bdc7138652b371792/5c84f31bdc7138652b371793 \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 9695590f-a30d-4099-86a6-68b2813c96e3' \
  -H 'X-Api-Key: 580515b376832580515b376887580515b3768dd' \
  -H 'cache-control: no-cache' \
  -d '{
	"payout": 4,
	"revenue": 20,
	"coverage": ["IN"]
}'
```

| Field | Type | Description | Nullable |
| --- | --- | --- | --- |
| payout | float | Payout of goal | Yes |
| revenue | float | Revenue of goal | Yes |
| coverage | array | public/private | Yes |

### **Response body parameters**

```json
{
    "success": true,
    "data": {
        "payout": [
            {
                "_id": "5c84f31bdc7138652b371793",
                "coverage": [
                    "IN"
                ],
                "revenue": 20,
                "payout": 4,
                "model": "fixed"
            }
        ],
        "message": "Payout Saved Successfully!!"
    }
}
```



