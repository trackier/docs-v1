# Edit an Advertiser

| **HTTP method** | End Point |
| :--- | :--- |
| **POST** | **/advertiser/{id}** |

## **Request body parameters**

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: cc5d7610-80aa-8f1b-983d-fc5712fcfb53" -d '{
  "name": "testUser",
  "live": false
}' "http://api.vnative.com/advertiser/{id}"
```

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| name | string | Name of the advertiser | No |
| username | string | Username of the advertiser | No |
| password | string | Password of the advertiser | No |
| phone | string | Phone number of the advertiser | No |
| country | string | Country of the advertiser | No |
| email | string | Updated Email | No |
| live | boolean | Disable enable account | No |
| currency | string | Supported values \["INR","PKR","AUD","EUR","GBP","TRY","USD","IDR","THB","MYR","PHP","VND","RUB","PLN"\] | No |
| zone | string | Any value from the table given [https://www.w3schools.com/php/php\_ref\_timezones.asp](https://www.w3schools.com/php/php_ref_timezones.asp) | No |

## **Response body parameters**

```javascript
{
  "success": true,
  "data": {
    "user": {
      "org_id": "string",
      "name": "Awesome User",
      "username": "#Awesome_user",
      "email": "abc@example.com",
      "password": "deb750c4f124a9ab6581b4537bc2cd680a17cb70",
      "phone": "string",
      "country": "IN",
      "currency": "USD",
      "type": "publisher",
      "login": null,
      "_id": "string",
      "live": false,
      "created": "2016-10-25",
      "modified": "2016-11-08",
      "meta": {
        "afields": {
          "skype_id": "live:test",
          "screenshot": "image.png"
        }
      }
    },
    "message": "Advertiser Updated!!"
  }
}
```

