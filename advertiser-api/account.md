# **Get Account Details**

| **HTTP method** | **End Point** | **Description** |
| --- | --- |
| GET | /advertiser/account | Get account details |
| PATCH | /advertiser/account | Edit account details |

## Get Details

### **Sample Request**

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" -H "Postman-Token: 0e0b686e-7911-32a4-c10b-99ceb8e45d28" "https://api.vnative.com/advertiser/account"
```

### **Response body**

```json
{
    "success": true,
    "data": {
        "postbacks": [],
        "invoices": [
            {
                "start": "2016-09-21",
                "end": "2016-10-30",
                "amount": 87.780452,
                "_id": "string",
                "live": true,
                "created": "2016-11-21"
            }
        ],
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
            "username": "Vnative",
            "name": "Vnative",
            "email": "string",
            "password": "d4fb9cfae097eb1912f336c194c9c20a861e4230",
            "phone": null,
            "country": "IN",
            "currency": "INR",
            "type": "advertiser",
            "login": null,
            "region": null,
            "_id": "string",
            "live": true,
            "created": "2016-08-28",
            "modified": "2016-12-19",
            "meta": []
        }
    }
}
```

## Edit Details

### **Sample Request**

```bash
curl -X PATCH -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: 67fdace5-1607-0a78-5482-dbd1160d0a01" -d '{
    "action": "password",
    "old_password": "dfjkl34D45F",
    "new_password": "somethingCool!!"
}' "https://api.vnative.com/advertiser/account"
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
        "postbacks": [],
        "errors": [],
        "message": "Password updated successfully!!",
        "invoices": [
            {
                "start": "2016-09-21",
                "end": "2016-10-30",
                "amount": 87.780452,
                "_id": "string",
                "live": true,
                "created": "2016-11-21"
            }
        ],
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
            "username": "Vnative",
            "name": "Vnative",
            "email": "string",
            "password": "8517d294f7410c7d8a7540491389faf6b0896e27",
            "phone": null,
            "country": "IN",
            "currency": "INR",
            "type": "advertiser",
            "login": "2016-12-26",
            "region": null,
            "_id": "string",
            "live": true,
            "created": "2016-08-28",
            "modified": "2016-12-26",
            "meta": []
        }
    }
}
```
