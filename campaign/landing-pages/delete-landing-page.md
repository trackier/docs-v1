## **Delete a goal**

| HTTP Method | End Point |
| --- | --- |
| DELETE | **/campaign/lpages/{CampaignID}/{LandingPageId}** |

### Response Body

```bash
curl -X DELETE \
  http://api.vnative.com/campaign/lpages/{CampaignID}/{LandingPageId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 7d0dbb13-864a-48ba-8fdd-d5cdbf992c6d' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache'
```

```json
{
    "success": true,
    "message": "Landing page deleted Successfully",
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

* Success - true when landing page is removed successfully

* Success - false when landing page can not be removed from the database



