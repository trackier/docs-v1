# Delete a Goal

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | /goal/{goal\_id} |

## Response Body

```bash
curl -X DELETE \
  http://restapi.trackier.io/goal/5d638445b6920d0947195996 \
  -H 'X-Api-Key: {API_KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "message": "Goal removed from database!!"
    }
}
```

* Success - true when goal is removed successfully
* Success - false when goal can not be removed from the database

