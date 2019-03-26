# Edit an Affiliate

| **HTTP method** | End Point |
| :--- | :--- |
| **POST** | **/affiliate/{id}** |

## **Request body parameters**

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: cc5d7610-80aa-8f1b-983d-fc5712fcfb53" -d '{
  "name": "testUser",
  "live": false
}' "http://api.vnative.com/affiliate/{id}"
```

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| name | string | Name of the affiliate | No |
| username | string | Username of the affiliate | No |
| password | string | Password of the affiliate | No |
| phone | string | Phone number of the affiliate | No |
| country | string | Country of the affiliate | No |
| live | boolean | Disable enable account | No |
| email | string | Updated email of affiliate | No |
| zone | string | Any value from the table given [https://www.w3schools.com/php/php\_ref\_timezones.asp](https://www.w3schools.com/php/php_ref_timezones.asp) | No |
| currency | string | Supported values \["INR","PKR","AUD","EUR","GBP","TRY","USD","IDR","THB","MYR","PHP","VND","RUB","PLN"\] | No |
| bank\*\* | object | Stores the affiliate bank related info | No |
| meta\_payout\*\* | object | Stores the payout related info | No |

### Sample Field Values\*\*

If These objects are provided then they are replaced with the new object given in the request

_a\) Bank Object_

```javascript
"bank": {
    "name": "State Bank of India",
    "ifsc": "SBIN00xxxx",
    "account_no": "112322442",
    "account_owner": "Test User"
  }
```

_b\) Meta Payout object_

```javascript
"meta_payout": {
    "paypal": "",
    "payquicker": "",
    "payoneer": "PAY-4452243",
    "paytm": "",
    "easypaisa": "",
    "mobicash": ""
}
```

## **Response body parameters**

```javascript
{
    "success": true,
    "data": {
        "affiliate": {
            "display_id": 23,
            "org_id": "57c4718434243dc47d8b456b",
            "manager_id": null,
            "username": "PubsTest",
            "name": "Pubs Test",
            "email": "pubs@vnative.com",
            "password": "d4fb9cfae097eb1912f336c194c9c20a861e4230",
            "phone": "9958636932",
            "country": null,
            "type": "publisher",
            "tier_id": null,
            "login": null,
            "login_attempts": null,
            "region": {
                "currency": "INR",
                "zone": "Europe/London",
                "lang": "en"
            },
            "deleted": false,
            "_id": "5980a682b6920d5a4e362550",
            "live": true,
            "created": "2017-08-01",
            "modified": "2017-11-12",
            "meta": {
                "afields": {
                    "fb_page_url": "https://fb.com/officialvnative",
                    "page_screenshot": "5980a68201e50.png"
                },
                "payout": {
                    "paypal": "paypal.me/myuniqId",
                    "payquicker": "",
                    "payoneer": "PAY-4452243",
                    "paytm": "",
                    "easypaisa": "",
                    "mobicash": ""
                },
                "bank": {
                    "name": "State Bank of India",
                       "ifsc": "SBIN00xxxx",
                        "account_no": "112322442",
                        "account_owner": "Test User"

                }
            },
            "status": "active"
        },
        "message": "Affiliate Updated!!"
    }
}
```

