# Create a Commission

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/commissions/{campId}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| rate | float | Amount charged from advertiser in Network Currency | No |
| revenue | float | Amount paid to affiliate in Network Currency | No |
| coverage | array | Array of country codes can be found from dictionary: _\(Default -&gt; \['ALL'\]\)_ | Yes |

### Example Request

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{
    "coverage": ["IN", "US"],
    "rate": 0.23,
    "revenue": 0.35
}' "https://api.trackier.com/commissions/{campId}"
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "commission": {
            "ad_id": "{campId}",
            "model": "cpa",
            "revenue": 0.35,
            "rate": 0.23,
            "coverage": [
                "IN",
                "US"
            ],
            "_id": "{id}",
            "created": "2016-10-09",
            "modified": null
        },
        "message": "Commission Saved Successfully!!"
    }
}
```

