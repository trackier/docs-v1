## Update** an existing goal**

| **HTTP method** | **EndPoint** |
| --- | --- |
| POST | /goal/{goalId} |

### **Request body parameters**

```bash
curl -X POST \
  http://api.vnative.com/goal/{goalId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 768c47f6-4bff-425a-aa95-b38bd19d7177' \
  -H 'X-Api-Key: 580515b376832580515b376887580515b3768dd' \
  -H 'cache-control: no-cache' \
  -d '{
    "title": "Api Test Goal Update",
    "value": 200,
    "model": "fixed",
    "type": "public"
}'
```

| Field | Type | Description | Nullable |
| --- | --- | --- | --- |
| title | string | Goal name | Yes |
| value | string | Goal value | Yes |
| type | string | public/private | Yes |
| model | string | fixed/percentage | Yes |

### **Response body parameters**

```json
{
    "success": true,
    "data": {
        "goal": {
            "_id": "5c84a6b5dc7138652c44fad2",
            "title": "Api Test Goal Update",
            "value": "200",
            "type": "public"
        },
        "message": "Goal updated Successfully!!"
    }
}
```



