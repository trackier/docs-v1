# List all Commission

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /commissions/{campId} | Display all the commissions |
| GET | /commissions/{campId}/{id} | Display info of a single commissions |

## Response body

Revenue is what is charged from advertiser and rate is what is given to the affiliate

* _**For all the commissions**_

  ```bash
  curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/commissions/{campId}"
  ```

```javascript
{
    "success": true,
    "data": {
        "commissions": [
            {
                "ad_id": "{campId}",
                "description": null,
                "model": "cpa",
                "revenue": 1.5151,
                "rate": 0.1515,
                "coverage": [
                    "ALL"
                ],
                "_id": "{id}",
                "created": "2016-10-08",
                "modified": null
            },
            {
                "ad_id": "{campId}",
                "description": "Another Commission",
                "model": "cpa",
                "revenue": 2.6151,
                "rate": 1.1515,
                "coverage": [
                    "ALL"
                ],
                "_id": "{id}",
                "created": "2016-10-08",
                "modified": null
            }
        ]
    }
}
```

* _**For a single commissions**_

  ```bash
  curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/x-www-form-urlencoded" -H "Cache-Control: no-cache" "http://api.vnative.com/commissions/{campId}/{id}"
  ```

```javascript
{
    "success": true,
    "data": {
        "commission": {
            "ad_id": "{campId}",
            "description": null,
            "model": "cpa",
            "revenue": 1.5151,
            "rate": 0.15151,
            "coverage": [
                "ALL"
            ],
            "_id": "{id}",
            "created": "2016-10-08",
            "modified": null
        }
    }
}
```

