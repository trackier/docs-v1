# **Create a commission**

| **HTTP method** | **End Point** |
| --- | --- |
| **POST** | **/commissions/{campId}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| model | string | Payout Model -> cpa, cpc, cpv, cps, cpm | No
| description | string | What is this commission for? | Yes
| rate | float | Amount charged from advertiser in Network Currency | No
| revenue | float | Amount paid to affiliate in Network Currency | No
| coverage | array | Array of country codes can be found from dictionary: _(Default -> ['ALL'])_ | Yes

### Example Request

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -d '{
    "coverage": ["IN", "US"],
    "model": "cpc",
    "rate": 0.23,
    "revenue": 0.35,
    "description": "This is a test description"
}' "https://api.vnative.com/commissions/{campId}"
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



