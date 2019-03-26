## **Create a new advertiser**

| **HTTP method** | **EndPoint** |
| --- | --- |
| POST | /advertiser |

### **Request body parameters**

#### Note
If there are custom fields set in the network then all the **required** custom fields must be sent in the request

Example Custom fields
See - [Advertiser Custom Fields Dictionary](/dict/custom-fields/README.md)
```json
{
  "success": true,
  "data": {
    "fields": [
      {
        "label": "FB Page URL",
        "type": "text",
        "name": "fb_page_url",
        "required": true,
        "id": "5918b7cdb6920d1ccb35b2f5"
      },
      {
        "label": "Page Screenshot",
        "type": "file",
        "name": "page_screenshot",
        "required": true,
        "id": "5918b93fb6920d1d4a4dcd73"
      }
    ]
  }
}
```

```bash
curl -X POST -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" -H "Postman-Token: cc5d7610-80aa-8f1b-983d-fc5712fcfb53" -d '{
  "name": "Awesome User",
  "email": "test@gmail.com",
  "password": "somethingCool!!",
  "phone": "yo",
  "custom_fields": {
    "fb_page_url": "http://facebook.com/path",
    "page_screenshot": "http://demo.vnative.com/assets/img/logo.png"  
  }
}' http://api.vnative.com/advertiser
```

Here the format of *custom_fields* object is:
```json
{
  "custom_fields": {
    "fields.0.name": "value",
    "fields.1.name": "value"  // for a field.type: "file" => Send a link to the corresponding IMAGE/PDF file
  }
}
```

| Field | Type | Description | Nullable |
| --- | --- | --- | --- |
| name | string | Name of the advertiser | No |
| email | string | Email of the advertiser | No |
| password | string | Password of the advertiser | No |
| phone | string | Phone Number of the advertiser | Yes |
| country | string | Country \(Two letter country code\) | Yes |

### **Response body parameters**

```json
{
  "success": true,
  "data": {
    "user": {
      "org_id": "string",
      "username": "Awesome User",
      "name": "Awesome User",
      "email": "test@gmail.com",
      "password": "da39a3ee5e6b4b0d3255bfef95601890afd80709",
      "phone": "9998887776",
      "country": "IN",
      "currency": "USD",
      "type": "publisher",
      "login": null,
      "_id": "5821f9e81d41c86b2e664df3",
      "live": false,
      "created": "2016-11-08",
      "modified": null,
      "meta": []
    },
    "message": "Advertiser Added!!",
  }
}
```

