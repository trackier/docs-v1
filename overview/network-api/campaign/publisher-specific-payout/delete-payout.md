# Delete Payout

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | **/network/pub-payout/{PAYOUT-ID}** |

## Response Body

```bash
curl -X DELETE \
  http://api.trackier.com/network/pub-payout/{PAYOUT-ID} \
  -H 'Accept: */*' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Host: restapi.trackier.io' \
  -H 'Postman-Token: f85cc6ae-23ed-4ac9-9fa4-71d7cb6197f3,423d11c7-6829-4ca6-ae43-bd2de22f4869' \
  -H 'User-Agent: PostmanRuntime/7.13.0' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'accept-encoding: gzip, deflate' \
  -H 'cache-control: no-cache' \
  -H 'content-length: ' \
  -H 'cookie: __cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6' \
  -b '__cfduid=de429619278fbd4b65dbadb6a65cea3d41551186229; PHPSESSID=vosaiu4kd28qno7gkfm4gvl3k6'
```

```javascript
{
    "success": true,
    "message": "Publisher Specific Payout Deleted Successfully"
}
```

* Success - true when payout is removed successfully
* Success - false when payout can not be removed from the database

