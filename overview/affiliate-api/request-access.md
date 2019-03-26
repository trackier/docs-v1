# Campaign Access

| **HTTP method** | **End Point** |
| :--- | :--- |
| GET | /affiliate/requestAccess/{campaignId} |

## **Sample Request**

When Sending a request to this endpoint access will be requested to run a campaign if not already requested!!

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "https://api.vnative.com/affiliate/requestAccess/{campaignId}"
```

### **Response body**

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

