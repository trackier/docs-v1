# Update** a Landing Page**

| **HTTP method** | **End Point** |
| --- | --- |
| **POST** | **/campaign/lpages/{CampaignID}/{LandingPageId}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title | string | Title of landing page | Yes |
| preview\_url | string | Preview url to be displayed | Yes |
| url | string | Landing page redirect URL | Yes |

### Example Request

```bash
curl -X POST \
  http://api.vnative.com/campaign/lpages/{CampaignID}/{LandingPageId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 016750c4-c098-440b-88c9-167cdad22b63' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
     "title": "Test URL",
     "preview_url": "http://www.fac.com",
     "url": "http://www.fac.com"
}'Response body
```

```json
{
    "success": true,
    "message": "Landing page updated Successfully",
    "data": {
        "landing_pages": [
            {
                "_id": "5b7e9972b6920d55f25a6ec7",
                "modified": null,
                "int_id": 2,
                "title": "Testing 2",
                "preview_url": "http://www.fakingnews.com/vids/sweet-life-atta-boys-ac-repair-s01e01-27217",
                "url": "http://www.fakingnews.com/vids/sweet-life-atta-boys-ac-repair-s01e01-27217"
            },            
            {
                "_id": "5c18ca3f89d446551f622074",
                "modified": {
                    "date": "2018-12-18 10:26:51.860000",
                    "timezone_type": 1,
                    "timezone": "+00:00"
                },
                "int_id": 5,
                "title": "Test URL",
                "preview_url": "http://www.fac.com",
                "url": "http://www.fac.com"
            }
        ]
    }
}
```



