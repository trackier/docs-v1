# Delete Goal

|  | **End Point** |
| :--- | :--- |
| DELETE | /goal/{goalId} |

## Response Body

```bash
curl -X DELETE \
  http://api.vnative.com/goal/5c84a6b5dc7138652c44fad2 \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 4a6ee42d-baca-42be-8fb4-4aae07047f23' \
  -H 'X-Api-Key: {API-KEY}' \
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

