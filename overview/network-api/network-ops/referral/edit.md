# Edit a referral link

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| PATCH | /network/referral/{id} |

## **Example request**

```bash
curl -X PATCH \
  https://api.trackier.com/network/referral \
  -H 'content-type: application/json' \
  -H 'postman-token: 71bc684a-ba03-dd3c-34b5-792f34ec39c7' \
  -H 'x-api-key: {apiKey}' \
  -d '{
    "live": false
}'
```

### Request body Params

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| publisher\_id | string | Id of the publisher | Yes |
| recurring | boolean | Whether the publisher will receive recurring commission | No |
| base | string | Acceptable values - \(payout, profit\) whether commission is based on the payout of the registering affiliate or the profit made by the affiliate to the network | No |
| type | string | Commission type - percentage or fixed amount Values -&gt; \(percentage, amount\) | No |
| rate | float | Rate corresponding to the commission type, in case of percentage it wil be treated as percent \(i.e. rate = 10, base = profit, 10 % of the profit\) | No |
| live | boolean | Enable / Disable the referral link | No \(default: true\) |

## **Example response**

```javascript
{
    "success": true,
    "data": {
        "referral": {
          "user_id": "57e262141d41c81f2b04b8d0",
          "recurring": true,
          "type": "percentage",
          "base": "profit",
          "rate": 30,
          "_id": "5925763489d4467dfe50d337",
          "live": false,
          "created": "2017-05-24 17:31:56",
          "modified": "2017-05-24 17:43:59"
        },
        "message": "Referral link Updated!!",
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

