# Create a Landing Page

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/campaign/lpages/{CampaignID}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title | string | Title of landing page | No |
| preview\_url | string | Preview url to be displayed | No |
| url | string | Landing page redirect URL | No |

### Example Request

```bash
curl -X POST \
  http://api.vnative.com/campaign/lpages/{CampaignID} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: ba325a5a-188a-4901-bca4-f9f2e8a91c2a' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
     "title": "Fac URL",
     "preview_url": "http://www.fac.com",
     "url": "http://www.fac.com"
}'
```

### **Response body**

```javascript
{
    "success": true,
    "message": "Landing page added Successfully",
    "data": {
        "landing_pages": [
            {
                "_id": "5a095cf4b6920d156e780efa",
                "modified": {
                    "date": "2018-12-18 07:38:28.254000",
                    "timezone_type": 1,
                    "timezone": "+00:00"
                },
                "int_id": 1,
                "title": "Test URL",
                "preview_url": "http://www.fb.com",
                "url": "http://www.facebook.com"
            },
            {
                "_id": "5c18ca3f89d446551f622074",
                "modified": null,
                "int_id": 5,
                "title": "Fac URL",
                "preview_url": "http://www.fac.com",
                "url": "http://www.fac.com"
            }
        ]
    }
}
```

