# Create a new Category

| **HTTP method** | **EndPoint** |
| --- | --- |
| POST | /dictionary/categories |

### **Request body parameters**

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/x-www-form-urlencoded" -H "Cache-Control: no-cache" -d 'name=Entertainment' "http://api.vnative.com/dictionary/categories
```

| Field | Type | Description | Required |
| --- | --- | --- | --- |
| name | string | Name of the category | Yes |

### **Response body parameters**

```json
{
    "success": true,
    "data": {
        "category": {
            "_id": "string",
            "name": "Test category",
            "org_id": "string"
        },
        "message": "Category saved successfully!!"
    }
}
```



