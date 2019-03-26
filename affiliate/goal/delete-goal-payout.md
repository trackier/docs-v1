## **Delete goal payout **

|  | **End Point** |
| --- | --- |
| DELETE | /goal/payout/{goalId}/{PayoutID} |

### Response Body

```bash
curl -X DELETE \
  http://restapi.trackier.io/goal/payout/5c84f31bdc7138652b371792/5c84f7ebdc7138652c44fad4 \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: d404f0bb-f065-453f-9557-c5a76d9e8d1c' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```json
{
    "success": true,
    "data": {
        "message": "Payout removed successfully!!"
    }
}
```

* Success - true when payout is removed successfully
* Success - false when payout can not be removed from the database



