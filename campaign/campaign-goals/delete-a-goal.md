## **Delete a goal \(Deprecated\)**

| HTTP Method | End Point |
| --- | --- |
| DELETE | /goals/{campId}/{goalId} |

### Response Body

```bash
curl -X DELETE \
  https://api.vnative.com/goals/{campaignId}/{goalId} \
  -H 'Content-Type: application/json' \
  -H 'Postman-Token: 48185b71-6efd-4722-bbff-845718c057a6' \
  -H 'cache-control: no-cache' \
  -H 'x-api-key: {API-KEY}'
```

```json
    "success": boolean,
    "data": {
        "message": "message"
    }
}
```

* Success - true when goal is removed successfully

* Success - false when goal can not be removed from the database



