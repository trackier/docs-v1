# **Update a commission**

| **HTTP method** | **End Point** |
| --- | --- |
| **POST** | **/commissions/{campId}/{id}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| model | string | Payout Model -> cpa, cpc, cpv, cps, cpm | Yes
| description | string | What is this commission for? | Yes
| rate | float | Amount charged from advertiser in Network Currency | Yes
| revenue | float | Amount paid to affiliate in Network Currency | Yes
| coverage | array | Array of country codes can be found from dictionary | Yes

### Example Request

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{
    "description": "This is a test description",
    "coverage": ["IN", "US"]
}' "https://api.vnative.com/commissions/{campId}/{id}"
```

### **Response body**

```json
{
    "success": true,
    "data": {
        "commission": {
            "ad_id": "{campId}",
            "description": "This is a test description",
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



