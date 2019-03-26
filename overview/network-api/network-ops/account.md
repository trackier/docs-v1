# Account

## About the logged in Network

| **HTTP METHOD** | **End Point** | Description |
| :--- | :--- | :--- |
| GET | /network/account | List the Network Details |
| PATCH | /network/account | Edit the Network Details |

## GET Details

### Sample Request

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" "https://api.vnative.com/network/account"
```

### Response Body

```javascript
{
    "success": true,
    "data": {
        "currencyCodes": [
            "INR",
            "USD",
            "PKR",
            "AUD",
            "EUR",
            "GBP"
        ],
        "network": {
            "name": "Test",
            "domain": "demo",
            "url": "demo.vnative.com",
            "appearance": {
                "email": "info@vnative.com",
                "support": "",
                "termsurl": "",
                "hlogo": ""
            },
            "region": {
                "currency": "USD",
                "zone": "Asia/Kolkata"
            },
            "_id": "57c4718434243dc47d8b456b",
            "live": true,
            "created": "2016-10-06",
            "modified": "2017-01-29",
            "meta": {
                "bill": {
                    "mic": "",
                    "tcc": ""
                },
                "widgets": [
                    "top10pubs",
                    "top10ads"
                ],
                "widget": {
                    "top10pubs": [
                        {
                            "_id": "57e262141d41c81f2b04b8d0",
                            "username": "test pub",
                            "count": 2
                        },
                        {
                            "_id": "585306ddb6920d048c717594",
                            "username": "#testing_demo_account",
                            "count": 1
                        }
                    ],
                    "top10ads": [
                        {
                            "_id": "587d16efb6920d7107695620",
                            "clicks": 1
                        },
                        {
                            "_id": "57f88e761d41c80ec577f11f",
                            "clicks": 1
                        },
                        {
                            "_id": "58884efcb6920d38c60a7ca2",
                            "clicks": 1
                        }
                    ]
                }
            }
        }
    }
}
```

## Edit Details

### **Sample Request**

```bash
curl -X PATCH -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 080b2b96-5d26-c632-1c6d-d9d05e3393a1" -d '{
    "name": "Changing Blah",
    "email": "account@somedomain.com",
    "support": "http://somedomain.com/path/to/support/link",
    "termsurl": "http://somedomain.com/path/to/terms-and-conditions",
    "currency": "USD"
}' "https://api.vnative.com/network/account"
```

| Fields | Description | Type | Nullable |
| :--- | :--- | :--- | :--- |
| name | Network Name | string | Yes |
| url | Network URL | string | Yes |
| email | Network Support email | string | Yes |
| support | Network Support Link | string | Yes |
| termsurl | Network Terms and conditions link | string | Yes |
| currency | Network currency | string | Yes |

### **Response Body**

```javascript
{
    {
    "success": true,
    "data": {
        "currencyCodes": [
            "INR",
            "USD",
            "PKR",
            "AUD",
            "EUR",
            "GBP"
        ],
        "network": {
            "name": "Changing Blah",
            "domain": "demo",
            "url": "demo.vnative.com",
            "appearance": {
                "email": "account@somedomain.com",
                "support": "http://somedomain.com/path/to/support/link",
                "termsurl": "http://somedomain.com/path/to/terms-and-conditions",
                "hlogo": "589057bd1f95c.png",
                "logo": "58904730b5f92.png"
            },
            "region": {
                "currency": "INR",
                "zone": "Asia/Kolkata"
            },
            "_id": "{id}",
            "live": true,
            "created": "2016-10-17",
            "modified": "2017-02-07",
            "meta": {}
        }
    }
}
}
```

