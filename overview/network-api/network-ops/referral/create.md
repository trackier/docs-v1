# Create new referral link

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /network/referral |

## **Example request**

```bash
curl -X POST \
  https://api.vnative.com/network/referral \
  -H 'content-type: application/json' \
  -H 'postman-token: 71bc684a-ba03-dd3c-34b5-792f34ec39c7' \
  -H 'x-api-key: {apiKey}' \
  -d '{
    "publisher_id": "{userId}",
    "recurring": true,
    "base": "profit",
    "type": "percentage",
    "rate": "30"
}'
```

### Request body Params

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| publisher\_id | string | Id of the publisher | Yes |
| recurring | boolean | Whether the publisher will receive recurring commission | No \(default: true\) |
| base | string | Acceptable values - \(payout, profit\) whether commission is based on the payout of the registering affiliate or the profit made by the affiliate to the network | No \(Default: "payout"\) |
| type | string | Commission type - percentage or fixed amount Values -&gt; \(percentage, amount\) | No \(default: "percentage"\) |
| rate | float | Rate corresponding to the commission type, in case of percentage it wil be treated as percent \(i.e. rate = 10, base = profit, 10 % of the profit\) | No \(Default: 0.0\) |

## **Example response**

```javascript
{
    "success": true,
    "data": {
        "message": "Referral Link Created!!",
        "referral": {
            "user_id": "string",
            "recurring": true,
            "type": "percentage",
            "base": "profit",
            "rate": 30,
            "_id": "string",
            "live": true,
            "created": "2017-05-24 17:31:56",
            "modified": null
        },
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

