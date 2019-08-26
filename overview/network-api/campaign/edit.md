# Update a Campaign

**Edit a campaign**

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/campaign/{id}** |

| Action | Fields | Type | Required |
| :--- | :--- | :--- | :--- |
| **targeting** |  |  |  |
|  | device | array \(mobile/ tablet/ desktop/ all\) | No |
|  | os | array \(android/ios/all\) | No |
|  | visibility | string - \(public or private or permission\) | No |
| **image\_upload** |  |  |  |
|  | image\_url | url | Yes |
| **basic\_info** |  |  |  |
|  | title | string | No |
|  | url | url | No |
|  | preview\_url | url | No |
|  | description | string | No |
|  | expiry | string \(date: Y-M-D\) | No |
|  | live | boolean | No |
|  | category | array | No |
|  | status | string | No |
|  | model | string\(cpa, cps, cpm, cpl, cpi, cpc\) | No |

## **Request body parameters**

```javascript
{
    "action": "targeting",
    "device": ["andriod", "iphone"],
    "category": ["id1", "id2"],
    "visibility": "public",
    "permission": false
}
```

* Category ID's can be found from the dictionary
* Devices can be found using dictionary

## Example Request

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 54faa9bd-949f-f512-8bfd-2e7af2742b9f" -d '{
    "action": "targeting",
    "device": ["andriod", "iphone"],
    "category": ["{id1}", "{id1}"],
    "visibility": "public",
    "permission": false
}' "https://api.vnative.com/campaign/{id}"
```

## **Response body**

```javascript
{
    "success": true,
    "data": {
        "campaign": {
            "user_id": "string",
            "org_id": "string",
            "title": "Deep Link Demo - Android Apps on Google Play",
            "description": "Deep Link Demo App",
            "url": "https://play.google.com/store/apps/details?id=xyz.abhaychauhan.www.deeplink&referrer=utm_source%3D123%26utm_medium%3Dblogslog&vnclick_id={click_id}",
            "preview_url": "https://play.google.com/store/apps/details?id=xyz.abhaychauhan.www.deeplink",
            "creative": null,
            "image": "5852549669438.jpg",
            "category": [
                "Technology",
                "Electric products"
            ],
            "type": "article",
            "device": [
                "andriod",
                "iphone"
            ],
            "expiry": null,
            "_id": "string",
            "live": true,
            "created": "2016-12-15",
            "modified": "2016-12-25",
            "meta": []
        },
        "message": "Targeting Info Updated!!"
    }
}
```

