# Remove an Affiliate

| **HTTP Method** | **End Point** |
| :--- | :--- |
| DELETE | /affiliate/{id} |

## Response Body

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.trackier.com/affiliate/{id}"
```

```javascript
{
    "data": {
        "message": "string"
    },
    "success": boolean
}
```

* Success - true when affiliate is removed successfully
* Success - false when affiliate can not be removed from the database

