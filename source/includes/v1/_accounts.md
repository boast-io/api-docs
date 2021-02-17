# Accounts

## Get All Accounts

> Request

```
GET http://api.boast.io/v1/accounts
```

> Response

```json
{
  "data": [
    {
      "id": "7a2f1f8c-7771-47e2-8dbd-332b301028a8",
      "name": "My Boast Account",
      "created_at": "2021-01-12T14:17:28.715Z",
      "updated_at": "2021-02-16T17:58:38.804Z"
    }
  ]
}
```

This endpoint retrieves all your accounts.

### HTTP Request

`GET http://api.boast.io/v1/accounts`

<aside class="notice">
Only accounts with API access enabled will appear in the list.
</aside>

## Get a Specific Account

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8
```

> Response

```json
{
  "data": {
    "id": "7a2f1f8c-7771-47e2-8dbd-332b301028a8",
    "name": "My Boast Account",
    "created_at": "2021-01-12T14:17:28.715Z",
    "updated_at": "2021-02-16T17:58:38.804Z"
  }
}
```

This endpoint retrieves all your accounts.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{id}`
