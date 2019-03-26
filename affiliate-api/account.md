# **Get Account Details**

| **HTTP method** | **End Point** | **Description** |
| --- | --- |
| GET | /affiliate/account | Get account details |
| PATCH | /affiliate/account | Edit account details |

## Get Details

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: c5d70184-208f-4423-6003-9e30f38c5087" "https://api.vnative.com/affiliate/account"
```

### **Response body**

```json
{
    "success": true,
    "data": {
        "postbacks": [
            {
                "org_id": "string",
                "user_id": "string",
                "ad_id": null,
                "event": "click",
                "data": "http://requestb.in/172a1kp1",
                "type": "url",
                "_id": "string",
                "live": true,
                "created": "2016-12-21",
                "modified": "2016-12-21",
                "meta": []
            }
        ],
        "invoices": [],
        "payments": [],
        "network": {
            "name": "Test",
            "domain": "demo",
            "url": "demo.vnative.com",
            "region": {
                "currency": "USD",
                "zone": "Asia/Kolkata"
            },
            "appearance": {
                "email": "info@vnative.com",
                "support": "",
                "termsurl": "",
                "hlogo": "",
                "logo": "",
            },
            "created": "2016-10-06"
        },
        "user": {
            "org_id": "string",
            "username": "demo",
            "name": "Demo Account",
            "email": "user@email",
            "password": "03aa85cad0cd378e1ce36e0e12e34910b8e3b06f",
            "phone": "333424333",
            "country": "IN",
            "currency": "USD",
            "type": "publisher",
            "login": "2016-12-21",
            "region": null,
            "_id": "string",
            "live": true,
            "created": "2016-10-21",
            "modified": "2016-12-31",
            "meta": {
                "afields": {
                    "skype_id": "live:something",
                    "screenshot": "584afd536762d.png"
                }
            }
        },
    }
}
```

## Edit Details

### **Sample Request**

```bash
curl -X PATCH -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 1e8f0c73-2448-e823-5224-3c3d8f08f465" -d '{
    "action": "basic_info",
    "name": "Testing Demo Account",
    "username": "#testing_demo_account"
}' "https://api.vnative.com/affiliate/account"
```

| Actions | Fields | Type | Required |
| :--- | :--- | :--- | :--- |
| password |  |  |  |
|  | old_password | string | Yes |
|  | new_password | string | Yes |
| basic\_info |  |  |  |
|  | name | string | No |
|  | phone | string | No |
|  | currency | string | No |
|  | username | string | No |

### **Response Body**

```json
{
    "success": true,
    "data": {
        "invoices": [
            {
                "_id": "string",
                "start": "2016-11-30",
                "end": "2016-12-08",
                "amount": 2.16,
                "live": false,
                "created": "2016-12-17"
            }
        ],
        "payments": [],
        "user": {
            "org_id": "string",
            "username": "#testing_demo_account",
            "name": "Testing Demo Account",
            "email": "user@email",
            "password": "03aa85cad0cd378e1ce36e0e12e34910b8e3b06f",
            "phone": "333424333",
            "country": "IN",
            "currency": "USD",
            "type": "publisher",
            "login": "2016-12-21",
            "region": null,
            "_id": "string",
            "live": true,
            "created": "2016-10-21",
            "modified": "2016-12-31",
            "meta": {
                "afields": {
                    "skype_id": "live:something",
                    "screenshot": "584afd536762d.png"
                }
            }
        },
        "network": {
            "name": "Test",
            "domain": "demo",
            "url": "demo.vnative.com",
            "region": {
                "currency": "USD",
                "zone": "Asia/Kolkata"
            },
            "appearance": {
                "email": "info@vnative.com",
                "support": "",
                "termsurl": "",
                "hlogo": "",
                "logo": "",
            },
            "created": "2016-10-06"
        },
        "postbacks": [
            {
                "user_id": "string",
                "ad_id": null,
                "event": "conversion",
                "data": "http://requestb.in/187ahha1?aff_p1={p1}&country={country_id}&browser={agent}&ref={referer}&affiliate={aff_id}&affiliate_name={aff_name}&username={aff_username}&ad={campaign_title}&advertiser={adv_id}&ipaddr={ip}&time={click_time}",
                "type": "url",
                "_id": "string",
                "live": true,
                "created": "2016-12-28",
                "modified": "2016-12-28"
            }
        ]
    }
}
```
