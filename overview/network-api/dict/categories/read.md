# List all categories

| **HTTP METHOD** | **End Point** |
| :--- | :--- |
| GET | /dictionary/categories |

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" "https://api.trackier.com/dictionary/categories"
```

## Response Body

```javascript
{
    "success": true,
    "data": {
        "categories": [
            {
                "_id": "string",
                "name": "Technology",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Hot",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Entertainment ",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Sports",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Lifestyle and food",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Politics ",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Fashion",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Electric products",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "News",
                "org_id": "string"
            },
            {
                "_id": "string",
                "name": "Test category",
                "org_id": "string"
            }
        ]
    }
}
```

