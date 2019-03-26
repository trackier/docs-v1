## **Delete a campaign**

| HTTP Method | End Point |
| --- | --- |
| DELETE | /campaign/{id} |

### Response Body

```bash
curl -X DELETE -H "X-Api-Key: {key}" -H "Cache-Control: no-cache" "http://api.vnative.com/campaign/{id}"
```

```json
{
    "data": {
        "message": "string",
    },
    "success": boolean
}
```

* Success - true when campaign is removed successfully

* Success - false when campaign can not be removed from the database



