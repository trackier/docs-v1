# List all landing pages

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /campaign/lpages/{CampaignID} | Display all Landing Pages |

## Response body

```bash
curl -X GET \
  http://api.vnative.com/campaign/lpages/{CampaignID} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: f412e9ed-1b26-43f0-bcfa-b315315027d3' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```javascript
    {
    "success": true,
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
                "_id": "5b7e9972b6920d55f25a6ec7",
                "modified": null,
                "int_id": 2,
                "title": "Testing 2",
                "preview_url": "http://www.fakingnews.com/vids/sweet-life-atta-boys-ac-repair-s01e01-27217",
                "url": "http://www.fakingnews.com/vids/sweet-life-atta-boys-ac-repair-s01e01-27217"
            },
            {
                "_id": "5b7e9986b6920d55f25a6ec8",
                "modified": null,
                "int_id": 3,
                "title": "Testing 3",
                "preview_url": "http://www.fakingnews.com/vids/",
                "url": "http://www.fakingnews.com/vids/sweet-life-atta-boys-ac-repair-s01e01-27217sldjflsdjf"
            },
            {
                "_id": "5bf5553cb6920d2cc35f4ea5",
                "modified": null,
                "int_id": 4,
                "title": "testing",
                "preview_url": "http://google.co.in",
                "url": "http://google.co.in?utm={click_id}"
            }
        ]
    }
}
```

