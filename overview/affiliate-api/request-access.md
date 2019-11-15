# Campaign Access

| **HTTP method** | **End Point** |
| :--- | :--- |
| POST | /affiliate/requestAccess/{campaignId} |

**Body Parameters**

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| message | string | Request Message for approval | Yes |

## **Sample Request**

When Sending a request to this endpoint access will be requested to run a campaign if not already requested!!

```bash
curl -X POST \
  https://api.vnative.com/affiliate/requestAccess/{campaignId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: e33caa07-c03b-4e46-8619-8ee5b17ba676' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "message": "Demo Message"
}'
```

On successful request there will be an access object containing the Request Access Id.

_The Live key will denote whether Affiliate has access to run this campaign or his/her access is revoked. If Access is revoked then the tracking link so generated in the process will be disabled!!_

```javascript
{
    "success": true,
    "data": {
        "message": "Access has already been requested!!",
        "access": {
            "_id": "{accessId}",
            "created": "2017-01-31",
            "live": false
        }
    }
}
```

