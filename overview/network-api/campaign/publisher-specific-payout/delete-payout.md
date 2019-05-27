# Delete Payout

| HTTP Method | End Point |
| :--- | :--- |
| DELETE | **/campaign/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID}** |

## Response Body

```bash
curl -X DELETE \
  http://api.trackier.com/campaign/pub-payout/{CAMPAIGN-ID}/{PAYOUT-ID} \
  -H 'Accept: */*' \
  -H 'Host: api.trackier.com' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'content-length: ' \
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

