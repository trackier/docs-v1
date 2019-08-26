# Update a Commission

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/commissions/{campId}/{id}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| rate | float | Amount charged from advertiser in Network Currency | Yes |
| revenue | float | Amount paid to affiliate in Network Currency | Yes |
| coverage | array | Array of country codes can be found from dictionary | Yes |

### Example Request

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{
    "rate": 4,
    "revenue: 10,
    "coverage": ["IN", "US"]
}' "https://api.vnative.com/commissions/{campId}/{id}"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "commission": {
            "ad_id": "{campId}",
            "model": "cpa",
            "revenue": 0.36,
            "rate": 0.26,
            "coverage": [
                "IN",
                "US"
            ],
            "_id": "{id}",
            "created": "2016-10-09",
            "modified": "2017-01-30"
        },
        "message": "Commission Updated!!"
    }
}
```

