# Create CAPs

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/caps/{campaignId}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">type</th>
      <th style="text-align:left">string</th>
      <th style="text-align:left">
        <ul>
          <li>conversion</li>
          <li>payout</li>
          <li>revenue</li>
          <li>click</li>
          <li>pendingPayout</li>
          <li>pendingRevenue</li>
          <li>approvedConv</li>
        </ul>
      </th>
      <th style="text-align:left">No</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| pub\_id \(Deprecated\) | string | Publisher Long ID | Yes |
| :--- | :--- | :--- | :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">pids</th>
      <th style="text-align:left">array</th>
      <th style="text-align:left">
        <p>Publisher Long ID&apos;s</p>
        <p>(For all publisher&apos;s send [&apos;ALL&apos;])</p>
      </th>
      <th style="text-align:left">No</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| daily | integer | Daily CAP limit | Yes |
| :--- | :--- | :--- | :--- |


| monthly | integer | Monthly CAP Limit | Yes |
| :--- | :--- | :--- | :--- |


| lifetime | integer | Lifetime CAP Limit | Yes |
| :--- | :--- | :--- | :--- |


| pc | integer | 0 - false/1 - true | Yes |
| :--- | :--- | :--- | :--- |


| geo | array | List of country codes | Yes |
| :--- | :--- | :--- | :--- |


| pub\_cap\_type | string | Publisher CAP Type \(each/group\) | Yes |
| :--- | :--- | :--- | :--- |


### Example Request

```bash
curl -X POST \
  http://api.vnative.com/caps/5c9dda0bb6920d6ac322a944 \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 65bfd287-5f37-43cf-afa6-c73552d2d24d' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "caps": [
        {
            "type":"revenue",
            "monthly": 30,
            "daily": 1,
            "lifetime":10000,
            "pc": 0,
            "pub_id": "5c9dca40b6920d57e15f1aa0",
            "geo": [
                "US", 
                "IN"    
            ]
        }
    ]
}'
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "caps": [
            {
                "pub_id": "5c9dca40b6920d57e15f1aa0",
                "ad_id": "5c9dda0bb6920d6ac322a944",
                "type": "revenue",
                "redirect": {
                    "type": "fallback_link"
                },
                "geo": [
                    "US",
                    "IN"
                ],
                "id": "5ca56391dc7138390a594866",
                "daily": 1,
                "monthly": 30,
                "lifetime": 10000,
                "pause_campaign": 0
            }
        ]
    },
    "message": "CAP Added Successfully"
}
```

