# Update a goal

| **HTTP method** | **End Point** |
| :--- | :--- |
| **POST** | **/goal/{goal\_id}** |

## Request Fields

| Field | Type | Description | Nullable |
| :--- | :--- | :--- | :--- |
| title | string | Goal Title | Yes |
| value | string | Goal Value | Yes |
| model | string | fixed/percentage | Yes |
| type | string | private/public/pub\_specific | Yes |
| whitelist\_pubs | Array of Int. | Publisher Short ID's/Display ID's | Yes |
| blacklist\_pubs | Array of Int. | Publisher Short ID's/Display ID's | Yes |

### Example Request

```bash
curl -X POST \
  http://restapi.trackier.io/goal/5d638445b6920d0947195996 \
  -H 'Content-Type: application/json' \
  -H 'X-Api-Key: {API_KEY}' \
  -H 'cache-control: no-cache' \
  -d '{
    "title": "API Goal",
    "value": "API_GOAL",
    "type": "private",
    "model": "percentage",
    "whitelist_pubs": [2, 4, 11],
    "blacklist_pubs": [6, 8]
}'
```

### **Response body**

```javascript
{
    "success": true,
    "data": {
        "goal": {
            "_id": "5d638445b6920d0947195996",
            "title": "API Goal",
            "value": "API_GOAL",
            "type": "private",
            "whitelist_pubs": [6, 8],
            "blacklist_pubs": [2, 4, 11]
        },
        "message": "Goal updated Successfully!!"
    }
}
```

