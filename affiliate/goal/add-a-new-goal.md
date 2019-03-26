## **Create a new goal**

| **HTTP method** | **EndPoint** |
| --- | --- |
| POST | /goal |

### **Request body parameters**

```bash
curl -X POST \
  http://api.vnative.com/goal \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: bdda301b-8d77-49a0-bd85-32f5f01ac785' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "goal": {
        "title": "Api Test Goal",
        "value": "api_test",
        "ad_id":"5cadefuay76aes2sadacaa"
        "type": "public",
        "model": "fixed"
    },
    "payouts": [
        {
            "payout": 2,
            "revenue": 10,
            "coverage": ["ALL"]
        }
    ]
}'
```

| Field | Type | Description | Nullable |
| --- | --- | --- | --- |
| title | string | Goal name | No |
| value | string | Goal value | No |
| ad\_id | string | Ad ID for Campaign Goal | Yes |
| type | string | public/private | No |
| model | string | fixed/percentage | Yes |

### **Response body parameters**

```json
{
    "success": true,
    "data": {
        "goal": {
            "_id": "5c84a6b5dc7138652c44fad2",
            "title": "Api Test Goal",
            "value": "api_test",
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
        ],
        "message": "Goal Saved Successfully!!"
    }
}
```



