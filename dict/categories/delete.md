# Delete a category

| **HTTP Method** | **End Point** |
| --- | --- |
| DELETE | /dictionary/categories/{id} |

### Example Request

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/dictionary/categories/{id}"
```

### Response Body

```json
{
    "data": {
        "message": "string"
    },
    "success": boolean
}
```

