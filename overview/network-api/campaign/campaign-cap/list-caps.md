# List CAPs

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /caps/{campId} | Display all the caps |
| GET | /caps/{campId}/{capId} | Display info of a single caps |

## Response body

* _**For all the caps**_

  ```bash
  curl -X GET \
    http://api.tarckier.com/caps/{CAMPAIGN-ID} \
    -H 'Content-Type: application/json' \
    -H 'Postman-Token: 89f9eeee-79b5-4668-9fd8-a4eccbc7b2d7' \
    -H 'X-Api-Key: {API-KEY}' \
    -H 'cache-control: no-cache'
  ```

```javascript
{
    "success": true,
    "data": {
        "caps": [
            {
                "pub_id": "ALL", (Deprecated)
                "pids": [
                    "ALL"
                ],
                "ad_id": "5c9dda0bb6920d6ac322a944",
                "type": "conversion",
                "redirect": {
                    "type": "blank",
                    "value": ""
                },
                "geo": [
                    "ALL"
                ],
                "id": "5ca30d60b6920d604d76746e",
                "daily": 10,
                "monthly": null,
                "lifetime": null,
                "pause_campaign": 1,
                "pub_cap_type": "each"
            },
            {
                "pub_id": "5c9dca40b6920d57e15f1aa0", (Deprecated)
                "pids": [
                    "5c9dca40b6920d57e15f1aa0"
                ]
                "ad_id": "5c9dda0bb6920d6ac322a944",
                "type": "revenue",
                "redirect": {
                    "type": "fallback_link"
                },
                "geo": [
                    "US",
                    "IN"
                ],
                "id": "5ca56391dc7138390a594866",
                "daily": 1,
                "monthly": 30,
                "lifetime": 10000,
                "pause_campaign": 0,
                "pub_cap_type": "group"
            }
        ]
    }
}
```

* _**For a single cap**_

  ```bash
  curl -X GET \
    http://api.tarckier.com/caps/{CAMPAIGN-ID}/{CAP-ID} \
    -H 'Content-Type: application/json' \
    -H 'Postman-Token: 222e809b-14ba-4216-87fe-ea9abe19d762' \
    -H 'X-Api-Key: {API-KEY}' \
    -H 'cache-control: no-cache'
  ```

```javascript
{
    "success": true,
    "data": {
        "caps": [
            {
                "pub_id": "ALL",
                "ad_id": "5c9dda0bb6920d6ac322a944",
                "type": "conversion",
                "redirect": {
                    "type": "blank",
                    "value": ""
                },
                "geo": [
                    "ALL"
                ],
                "id": "5ca30d60b6920d604d76746e",
                "daily": 10,
                "monthly": null,
                "lifetime": null,
                "pause_campaign": 1
            }
        ]
    }
}
```

