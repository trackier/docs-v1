# List all referral links

| **HTTP method** | End Point |
| :--- | :--- |
| GET | /network/referral |

## **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.trackier.com/network/referral"
```

## **Sample Response**

Here user\_id in each referral object represents the publisher ID i.e for which publisher this referral link will be used.

Eg: if referrals\[0\].\_id = HMN, then the referral link for the publisher will be

```bash
http://{domain}.trackier.com/publisher/register.html?referral=HMN
```

```javascript
{
    "success": true,
    "data": {
        "referrals": [
            {
                "user_id": "string",
                "recurring": true,
                "type": "percentage",
                "base": "profit",
                "rate": 30,
                "_id": "string",
                "live": true,
                "created": "2017-02-02 20:55:34",
                "modified": "2017-05-23 13:07:51",
                "signUps": 1
            },
            {
                "user_id": "string",
                "recurring": true,
                "type": "percentage",
                "base": "profit",
                "rate": 30,
                "_id": "string",
                "live": false,
                "created": "2017-05-24 17:31:56",
                "modified": "2017-05-24 17:44:52",
                "signUps": 0
            }
        ],
        "publishers": [
            {
                "_id": "string",
                "name": "Publisher Demo",
                "username": "#publisherDemo"
            },
            {
                "_id": "string",
                "name": "test pub",
                "username": "test pub"
            },
            {
                "_id": "string",
                "name": "Awesome User",
                "username": "Awesome User"
            }
        ]
    }
}
```

