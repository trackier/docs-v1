# Delete CAP

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | /caps/{campaignId}/{capId} |

## Response Body

```bash
curl -X DELETE \
  http://api.vnative.com/caps/{CAMPAIGN-ID}/{CAP-ID} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 5d02a0fc-ab7f-42a4-9273-8efa3bd29d79' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "message": "CAP removed from database!!"
    }
}
```

* Success - true when cap is removed successfully
* Success - false when cap can not be removed from the database

