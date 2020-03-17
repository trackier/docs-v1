# Create a new custom field

## Affiliates

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /dictionary/customField/affiliate |

### **Request Params**

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| fname | string | Field label | Yes |
| ftype | string | Type of field \(Supported values -&gt; text, file, date, email\) | No \(default: text\) |
| frequired | boolean | Whether the field is required | No \(default: true\) |

### **Sample Request**

```bash
curl --request POST --url https://api.trackier.com/dictionary/customField/affiliate --header 'content-type: application/json' --header 'x-api-key: {key}' --data '{
"fname": "Test custom field",
"ftype": "text",
"frequired": false
}'
```

### **Response body parameters**

```javascript
{
    "success": true,
    "data": {
        "message": "Added New Custom Field for affiliates"
    }
}
```

## Advertisers

| **HTTP method** | **EndPoint** |
| :--- | :--- |
| POST | /dictionary/customField/advertiser |

### **Request Params**

| Field | Type | Description | Required |
| :--- | :--- | :--- | :--- |
| fname | string | Field label | Yes |
| ftype | string | Type of field \(Supported values -&gt; text, file, date, email\) | No \(default: text\) |
| frequired | boolean | Whether the field is required | No \(default: true\) |

### **Sample Request**

```bash
curl --request POST --url https://api.trackier.com/dictionary/customField/advertiser --header 'content-type: application/json' --header 'x-api-key: {key}' --data '{
"fname": "adv custom field",
"ftype": "text",
"frequired": true
}'
```

### **Response body parameters**

```javascript
{
    "success": true,
    "data": {
        "message": "Added New Custom Field for advertisers"
    }
}
```

