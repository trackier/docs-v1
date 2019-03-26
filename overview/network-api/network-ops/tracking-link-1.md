# Create Tracking Link

| **HTTP method** | End Point | Description |
| :--- | :--- | :--- |
| GET | /network/link/{affiliate\_id}/{campaign\_id} | Get the Tracking link for a campaign |
| POST | /network/link/{affiliate\_id}/{campaign\_id} | Create a Tracking link for a campaign |

## **Get the Tracking Link**

Sending a request to this endpoint will display the tracking link if exists

### **Response body parameters**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 495264a7-dcbd-34b5-5e00-cf0a6b9d4884" "https://api.vnative.com/network/link/{affiliate_id}/{campaign_id}"
```

```javascript
{
    "success": true,
    "data": {
        "tracking_link": "http://dobolly.com/587dbed6b6920d496f7b5f2f",
        "link": {
            "user_id": "580a45201d41c82966347b8b",
            "ad_id": "587d16efb6920d7107695620",
            "domain": "dobolly.com",
            "_id": "587dbed6b6920d496f7b5f2f",
            "live": false,
            "created": "2017-01-17",
            "modified": null,
            "meta": []
        }
    }
}
```

## **Create a New Tracking Link**

Sending a request to this endpoint will create a tracking link if it does not exists else will return the tracking link previously created

### Request body parameters

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 37bc9799-7a19-bcd6-6746-2e9552e02dfb" -d '{"domain": "viralarticlez.com"}' "https://api.vnative.com/network/link/{affiliate_id}/{campaign_id}"
```

#### POST Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| domain | string | The tracking domain to be displayed to the Affiliate {/campaign/domains} | Yes |

### **Response body parameters**

```javascript
{
    "success": false,
    "data": {
        "message": "Link already exists!!",
        "tracking_link": "http://dobolly.com/{id}",
        "link": {
            "user_id": {affiliateId},
            "ad_id": {campaingId},
            "domain": "dobolly.com",
            "_id": {id},
            "live": true,
            "created": "2016-10-08",
            "modified": null,
            "meta": [],
        }
    }
}
```

