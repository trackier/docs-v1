# **Tracking Domains**

| HTTP Method | End Point | Description |
| --- | --- | --- |
| GET | /campaign/domains | Get the tracking domains |
| PUT | /campaign/domains | Add or Delete the tracking domains |

## Get Tracking Domains

Sending a request to this endpoint will return the tracking domains of the network

### Sample Request and Response

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/campaign/domains"
```

```json
{
    "success": true,
    "data": {
        "domains": [
            "viralarticlez.com",
            "dobolly.com"
        ]
    }
}
```

## Update Tracking Domains

Sending a request to this endpoint will update the tracking domains list with the new list provided with the JSON body. Remember sending an empty array will remove all the previously added domains **SO BE CAREFUL**

### Sample Request and Response

#### Valid Request

```bash
curl -X PUT -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{"domains": ["dobolly.com", "bollyhype.com"]}' "https://api.vnative.com/campaign/domains"
```

```json
{
    "success": true,
    "data": {
        "message": "Please follow this guide to add tracking domain. http://vnative.com/add-custom-tracking-domain-ad-network/",
        "domains": [
            "dobolly.com",
            "bollyhype.com"
        ]
    }
}
```

#### Invalid Request

```bash
curl -X PUT -H "X-Api-Key: {ket}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{"domains": null}' "https://api.vnative.com/campaign/domains"
```

```json
{
    "success": false,
    "data": {
        "message": "Invalid Request Body!!",
        "domains": [
            "dobolly.com",
            "bollyhype.com"
        ]
    }
}
```



