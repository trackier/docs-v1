# Delete an Advertiser

| **HTTP Method** | **End Point** |
| :--- | :--- |
| DELETE | /advertiser/{id} |

## Response Body

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.trackier.com/advertiser/{id}"
```

```javascript
{
    "data": {
        "message": "string"
    },
    "success": boolean
}
```

* Success - true when advertiser is removed successfully
* Success - false when advertiser can not be removed from the database

