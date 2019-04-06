# Update CAPs

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/caps/{campId}/{capId}** |

## Request Fields

<table>
  <thead>
    <tr>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Nullable</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <ul>
          <li>conversion</li>
          <li>payout</li>
          <li>revenue</li>
          <li>click</li>
          <li>pendingPayout</li>
          <li>pendingRevenue</li>
          <li>approvedConv</li>
        </ul>
      </td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">pub_id</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Publisher Long ID</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">daily</td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Daily CAP limit</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">monthly</td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Monthly CAP Limit</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">lifetime</td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">Lifetime CAP Limit</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">pc</td>
      <td style="text-align:left">integer</td>
      <td style="text-align:left">0 - false/1 - true</td>
      <td style="text-align:left">Yes</td>
    </tr>
    <tr>
      <td style="text-align:left">geo</td>
      <td style="text-align:left">array</td>
      <td style="text-align:left">List of country codes</td>
      <td style="text-align:left">Yes</td>
    </tr>
  </tbody>
</table>### Example Request

```bash
curl -X POST \
  http://api.vnative.com/caps/{CAMPAIGN-ID}/{CAP-ID} \
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

