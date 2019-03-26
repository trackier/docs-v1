# Delete a Commission

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | /commissions/{campId}/{id} |

## Response Body

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/commissions/{campId}/{id}"
```

```javascript
{
    "data": {
        "message": "string",
    },
    "success": boolean
}
```

* Success - true when commission is removed successfully
* Success - false when commission can not be removed from the database

