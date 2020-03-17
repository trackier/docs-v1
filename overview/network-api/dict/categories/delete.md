# Delete a Category

| **HTTP Method** | **End Point** |
| :--- | :--- |
| DELETE | /dictionary/categories/{id} |

## Example Request

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.trackier.com/dictionary/categories/{id}"
```

## Response Body

```javascript
{
    "data": {
        "message": "string"
    },
    "success": boolean
}
```

