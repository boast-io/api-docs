# Sequences

## Get All Sequences

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/sequences
```

> Response

```json
{
  "data": [
    {
      "id": "2b83ab61-30ef-48d4-8029-e73f61717c0a",
      "collection_form_id": "a873bcdb-ae03-436a-8410-d5057b81db34",
      "enrollment_form_id": "2f2082e9-ad81-4c41-9cb9-eaa2de5790b4",
      "name": "Sudden Valley Development",
      "status": "active",
      "created_at": "2020-10-08T17:46:46.460Z",
      "updated_at": "2021-02-09T19:30:21.828Z"
    }
  ]
}
```

This endpoint retrieves all sequences for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/sequences`
