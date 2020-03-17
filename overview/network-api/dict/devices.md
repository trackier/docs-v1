# Devices

| **HTTP METHOD** | **End Point** |
| :--- | :--- |
| GET | /dictionary/devices |

```bash
curl -X GET -H "X-Api-Key: {key}" -H "Content-Type: application/json" -H "Cache-Control: no-cache" "https://api.trackier.com/dictionary/devices"
```

## Response Body

```javascript
{
    "success": true,
    "data": {
        "devices": {
            "all": "All",
            "android": "Android",
            "iphone": "iPhone",
            "winphone": "Windows Phone",
            "linux": "Linux",
            "windows": "Windows",
            "mac": "Mac OS",
            "ipad": "iPad"
        }
    }
}
```

