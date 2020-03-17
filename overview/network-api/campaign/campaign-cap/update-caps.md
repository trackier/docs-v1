# Update CAPs

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/caps/{campId}/{capId}** |

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
      <th style="text-align:left">Yes</th>
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


<table>
  <thead>
    <tr>
      <th style="text-align:left">pub_cap_type</th>
      <th style="text-align:left">string</th>
      <th style="text-align:left">
        <p>Publisher CAP Type i.e each|group</p>
        <p>(Default: group)</p>
      </th>
      <th style="text-align:left">Yes</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>```bash
curl -X POST \
  http://api.trackier.com/caps/{CAMPAIGN-ID}/{CAP-ID} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: e0ed3bdf-ddd4-45e6-a1d1-faea5f9b04b5' \
  -H 'X-Api-Key: {API-KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
            "type":"approvedConv",
            "monthly": 60,
            "daily": 2,
            "lifetime":20000,
            "pc": 1
}'
```

### **Response body**

```javascript
{
    "success": true,
    "message": "CAP Updated Successfully",
    "data": {
        "caps": [
            {
                "pub_id": "ALL",
                "ad_id": "5c9dda0bb6920d6ac322a944",
                "type": "approvedConv",
                "redirect": {
                    "type": "blank",
                    "value": ""
                },
                "geo": [
                    "ALL"
                ],
                "id": "5ca30d60b6920d604d76746e",
                "daily": 2,
                "monthly": 60,
                "lifetime": 20000,
                "pause_campaign": 1
            }
        ]
    }
}
```

