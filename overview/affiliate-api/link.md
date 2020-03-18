# Link

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| GET | /affiliate/link/{campaignId} | Get Tracking link for a campaign |
| POST | /affiliate/link/{campaignId} | Generate Tracking link for a campaign if affiliate has permission |

## **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: dcef3ea0-3581-213c-eb32-feb0e708f3ea" "https://api.trackier.com/affiliate/link/{campaignId}"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "tracking_link": {
            "url": "http://{domain}/{id}",
            "live": true
        }
    }
}
```

