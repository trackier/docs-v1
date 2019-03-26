# Delete a custom field

## Affiliates

| **HTTP Method** | **End Point** |
| :--- | :--- |
| DELETE | /dictionary/customField/affiliate/{id} |

### Example Request

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/dictionary/customField/affiliate/{id}"
```

### Response Body

```javascript
{
    "data": {
        "message": "string"
    },
    "success": false
}
```

## Advertisers

| **HTTP Method** | **End Point** |
| :--- | :--- |
| DELETE | /dictionary/customField/advertiser/{id} |

### Example Request

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/dictionary/customField/advertiser/{id}"
```

### Response Body

```javascript
{
    "data": {
        "message": "string"
    },
    "success": true
}
```

Success -&gt; boolean whether the request was successful or not

