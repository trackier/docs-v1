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
	"model": "percentage"
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
            "type": "private"
        },
        "message": "Goal updated Successfully!!"
    }
}
```

