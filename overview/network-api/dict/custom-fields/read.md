# List all custom fields

## Affiliate

| **HTTP METHOD** | **End Point** |
| :--- | :--- |
| GET | /dictionary/customField/affiliate |

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" "https://api.trackier.com/dictionary/customField/affiliate"
```

### Sample Response Body

```javascript
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
            },
            {
                "label": "Test Custom Field",
                "type": "text",
                "name": "test_custom_field",
                "required": false,
                "id": "5949fad489d4465b273c71b2"
            }
        ]
    }
}
```

## Advertisers

| **HTTP METHOD** | **End Point** |
| :--- | :--- |
| GET | /dictionary/customField/advertiser |

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" "https://api.trackier.com/dictionary/customField/advertiser"
```

### Sample Response Body

```javascript
{
    "success": true,
    "data": {
        "fields": [
            {
                "label": "TAX",
                "type": "text",
                "name": "tax",
                "required": true,
                "id": "590dfe43b6920d12db0627d2"
            },
            {
                "label": "Skype",
                "type": "text",
                "name": "skype",
                "required": true,
                "id": "5918b6f9b6920d1ca70bd6d2"
            }
        ]
    }
}
```

