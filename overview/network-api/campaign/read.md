# List all the Campaigns

| HTTP Method | End Point | Description |
| :--- | :--- | :--- |
| GET | /campaign | Display all the campaigns |
| GET | /campaign/{id} | Display all the info of a single campaign |

## Request Parameters

| Key | Value | Description | Required |
| :--- | :--- | :--- | :--- |
| active | integer \(0, 1\) | To display campaigns based on their status \(active or inactive\) | No \(Default: 1\) |
| limit | integer | The number of records to be displayed | Yes |
| page | integer | page number for the given limit | Yes |

## Response body

* _**For all the campaigns**_

  ```bash
  curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/campaign?active=1"
  ```

```javascript
{
  "data": {
    "campaigns": [
      {
        "_id": "string (24 characters)",
        "title": "string",
        "description": "string",
        "image": "image.jpeg",
        "url": "http://url-to-content.com/path/to/content",
        "device": [
          "all"
        ],
        "expiry": null,
        "created": "2016-09-19",
        "commissions": {
          "{commission_id}": {
            "model": "cpc",
            "rate": 1,
            "revenue": 0.15,
            "coverage": [
              "ALL"
            ]
          }
        }
      },
      {
        "_id": "string",
        "title": "string",
        "description": "string",
        "image": "image.png",
        "url": "http://www.somewebsite.com/2016/some-awesome-content",
        "device": [
          "all"
        ],
        "expiry": null,
        "created": "2016-09-28",
        "commissions": [
          {
            "model": "cpm",
            "_id": "58f233...",
            "rate": 0.001969696969697,
            "revenue": 0.0068181818181818,
            "coverage": [
              "ALL"
            ]
          }
        ]
      }
    ],
    "total": 2,
    "page": 1,
    "limit": 20
  }
}
```

* _**For a single campaign**_

  ```bash
  curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/x-www-form-urlencoded" -H "Cache-Control: no-cache" "http://api.vnative.com/campaign/{id}"
  ```

```javascript
{
  "data": {
    "campaign": {
      "_id": "string",
      "title": "string",
      "description": "string,
      "image": "img.png",
      "url": "http://something.com/signup/",
      "device": [
        "all"
      ],
      "expiry": null,
      "created": "2016-10-09"
    },
    "commissions": [
      {
        "model": "cpa",
        "_id": "string",
        "rate": 1.5151515151515,
        "revenue": 3.030303030303,
        "coverage": [
          "AU",
          "CA",
          "US"
        ]
      }
    ]
  }
}
```

