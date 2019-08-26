# Delete a Goal Payout

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | /goal/payout/{goal\_id}/{payout\_id} |

## Response Body

```bash
curl -X DELETE \
  http://api.trackier.com/goal/payout/{goal_id}/{payout_id} \
  -H 'X-Api-Key: {API_KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
{
    "success": true,
    "data": {
        "message": "Payout removed successfully!!"
    }
}
```

* Success - true when payout is removed successfully
* Success - false when payout can not be removed from the database

