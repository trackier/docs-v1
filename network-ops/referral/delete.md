## **Delete an affiliate referral link**

| **HTTP Method** | **End Point** |
| --- | --- |
| DELETE | /network/referral/{id} |


### Sample Request
```bash
curl -X DELETE https://api.vnative.com/network/referral/{id}
```

### Response Body
```json
{
    "success": true,
    "data": {
        "message": "string"
    }
}
```

* Success - true when link is removed successfully
* Success - false when link can not be removed from the database

