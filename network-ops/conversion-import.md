# Conversion Import

| **HTTP method** | End Point | Description |
| --- | --- | --- |
| POST | /network/conversion-import | Upload / Edit Conversions |

## Request Parameters

If request is sent without **click\_id **it will by default create a new conversion

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| conversion\_id | string \(24 character id\) | Trackier Conversion ID | No \(Yes when editing\) |
| campaign\_id | int or string | Either the numeric id or Trackier 24 character campaign id | Yes \(If creating new conversion\) |
| publisher\_id | string | Either the numeric id of Trackier 24 character publisher ID | Yes \(if creating new conversion\) |
| goal\_id | string | 24 character ID Goal ID associated with this campaign | No |
| txn\_id | string | Unique identifier provided | No |
| sub1 | string | Sub ID 1 | No |
| sub2 | string | Sub ID 2 | No |
| sub3 | string | Sub ID 3 | No |
| sub4 | string | Sub ID 4 | No |
| sale\_amount | float | Sale Amount for the campaign | No |
| payout | float | Payout for conversion | No |
| revenue | float | Revenue for conversion | No |
| currency | string | Default Value = USD | No |
| method | string | Default Value = acquisition \(Other Values - pixel, app\_install\) | No |
| ipaddr | string | IP address from which this conversion was requested | No |
| status | string | Default Value - approved \(Other value - cancelled, pending, rejected\) | No |
| created | string | Format = YYYY-MM-DD H:i:s \(The time for recording conversion will be considered according to network timezone\) | No |
| referer | string | To store the referring page | No |

### **Response body parameters**

```bash
curl -i -X POST \
   -H "X-Api-Key: {key}" \
   -H "Content-Type:application/json" \
   -d \
'{
  "conversions": [
    {
      "conversion_id":"57c6c75934243d930c8b4581",
      "status": "approved"
    },
    {
      "campaign_id": 86,
      "publisher_id": "57c6c75934243d930c8b4581",
      "payout": 2,
      "revenue": 4,
      "currency": "USD",
      "created": "2017-10-26 22:33:00"
    }
  ]
}' \
 'https://api.vnative.com/network/conversion-import'
```

#### Sample Response

```json
{
    "success": true,
    "data": {
        "message": "Job has been queued!!",
        "job": {
            "_id": "5c54073a89d4465d2d17cf96",
            "status": "pending",
            "created": {
                "date": "2019-02-01 08:45:46.850000",
                "timezone_type": 1,
                "timezone": "+00:00"
            }
        }
    }
}
```

This endpoint will create a background job which will be processed by the system. The status of the job can be viewed using the jobs endpoint

**\*Notes**

* Sale Amount will only be considered to calculate payout when the campaign objective is set **Sales**
* > Valid Sale Currencies = USD, INR, AUD, EUR, TRY, IDR, THB, MYR, PHP, VND, RUR, PLN
* If Goal ID is passed then payout will be defined by Goal
* If Both Goal ID and Sale Amount are given then conversion will be marked as **Sale**

* If Conversion ID is given then system tries to find conversion with given id and updates it if found
* If more than 10 errors are generated while importing the conversions then the process will be halted in between



