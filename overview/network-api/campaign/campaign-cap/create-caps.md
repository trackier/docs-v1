# Create CAPs

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/caps/{campaignId}** |

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
      <td style="text-align:left">No</td>
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
</table>### **Note:** One field is required in monthly, daily and lifetime.

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

