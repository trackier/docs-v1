## **Delete an affiliate**

| **HTTP Method** | **End Point** |
| --- | --- |
| DELETE | /affiliate/{id} |

### Response Body

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/affiliate/{id}"
```

```json
{
    "data": {
		"message": "string"
	},
    "success": boolean
}
```

* Success - true when affiliate is removed successfully
* Success - false when affiliate can not be removed from the database

