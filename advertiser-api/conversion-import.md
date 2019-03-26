# Conversion Logs Import

| **HTTP method** | **End Point** | **Description** |
| :--- | :--- | :--- |
| POST | [/advertiser/conversion-import](/advertiser-api/conversion-import.md) | Create Conversion log import task |

### **Sample Request**

```php
curl -X POST \
  https://api.vnative.com/advertiser/conversion-import \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 69111d0d-2e3b-44aaa-962c-993582228cea' \
  -H 'X-Api-Key: 586118d12b1333360c8d12b1822860c8d12aaaa' \
  -H 'cache-control: no-cache' \
  -d '{
    "conversions": [
        {
            "click_id": "5aae975a9b155cccddccefbe",
            "sub1": "vNative Test Import Using API",
            "custom_dimensions": {
                "first_name": "Testing",
                "last_name": "Last Name"
            }
        }
    ],
    "send_postback": true
}'
```

| Key | Type | Description | Nullable |
| :--- | :---: | :--- | :---: |
| conversions | Array \[ \] | Conversion Object Array as shown in above sample. | No |
| click\_id | String | Click Id of a conversion | No |
| custom\_dimensions | Object | You can add your custom dimensions here. | Yes |
| send\_postback | Boolean | When report ready send postback. | Yes |

### Sample **Response body**

```json
{
    "success": true,
    "data": {
        "message": "Job has been queued!!",
        "job": {
            "orgId": "57a4718a4243ac47db4a6b",
            "type": "import",
            "subType": "job_import_conversion_v2",
            "relatedObject": {
                "csvPath": "5c6f54a44d3fb.json",
                "sendPostback": "1"
            },
            "resource": "Conversion",
            "resourceId": null,
            "state": "pending",
            "logs": [],
            "_id": "5c2f5454333446229468a428",
            "live": false,
            "created": {
                "date": "2018-01-04 12:40:52.331000",
                "timezone_type": 1,
                "timezone": "+00:00"
            },
            "modified": null,
            "meta": {}
        }
    }
}
```



