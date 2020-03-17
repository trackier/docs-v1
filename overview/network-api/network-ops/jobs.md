# Jobs API

Using this API we can get information about the job

| **HTTP Method** | Endpoint | Description |
| :--- | :--- | :--- |
| GET | /jobs | Get Latest 50 Jobs |
| GET | /jobs/{id} | Get Info about a single job |

## Sample Request

```bash
curl -i -X GET -H "X-Api-Key: {key}" 'https://api.trackier.com/jobs/{id}'
```

## Sample Response

```javascript
{
    "success": true,
    "data": {
        "job": {
            "name": "import.json.conversion",
            "_id": "5c54073a89d4465d2d17cf96",
            "created": {
                "date": "2019-02-01 08:45:46.000000",
                "timezone_type": 1,
                "timezone": "+00:00"
            },
            "status": "completed"
        },
        "logs": [
            {
                "object": "import.csv.conversions",
                "priority": 1,
                "message": "Total Processed: 2 | Imported: 0 | Edited: 2 | Errors: 0",
                "_id": "5c540745b6920d54c3777554",
                "created": "2019-02-01 14:15:57"
            }
        ]
    }
}
```

**Notes**

* Job Status can be **pending, progress, completed, failed**
* Currently the latest 100 logs will be displayed when getting info about a single job

