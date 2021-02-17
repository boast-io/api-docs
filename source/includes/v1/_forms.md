# Forms

## Get All Forms

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/forms
```

> Response

```json
{
  "data": [
    {
      "id": "8e424fa5-94fd-4353-8bec-96ed7a4bbd1a",
      "name": "NPS",
      "status": "active",
      "created_at": "2021-01-27T18:54:22.972Z",
      "updated_at": "2021-02-04T21:58:51.125Z"
    }
  ]
}
```

This endpoint retrieves all forms for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/forms`
