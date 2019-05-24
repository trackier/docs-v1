---
description: Assign Publisher's to Private and Permission Campaigns
---

# Campaign Access

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /campaign/assign-publisher |

## **Request body example**

```bash
curl -X POST \
  https://api.trackier.com/campaign/assign-publisher \
  -H 'Accept: */*' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'Host: restapi.trackier.io' \
  -H 'Postman-Token: ff3d4264-49ec-4fe6-a9b9-a2d9821c5d26,71f3c0da-a1ae-429f-a398-98bbaa44c748' \
  -H 'User-Agent: PostmanRuntime/7.13.0' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'accept-encoding: gzip, deflate' \
  -H 'cache-control: no-cache' \
  -H 'content-length: 97' \
  -H 'cookie: __cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6' \
  -b '__cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6' \
  -d '{
	"publisher_ids": ["5c9dca40b6920d57e15f1aa0"],
	"campaign_ids": ["5c9dd7fcb6920d676c65b14d"]
}'
```

## Response Body

```javascript
{
    "data": {
        "message": "Campaign Access Granted",
    },
    "success": boolean
}
```

## **Request body parameters**

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| publisher\_ids | array | List of Publisher Long ID's | No |
| campaign\_ids | array | List of Campaign Long ID's | No |
|  |  |  |  |

