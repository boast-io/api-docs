# Webhook Subscriptions

## Get All Webhook Subscriptions

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/webhook_subscriptions
```

> Response

```json
{
  "data": [
    {
      "id": "cb836066-c343-4b0a-8516-dbd802567b92",
      "event_name": "response.status_changed",
      "filters": {
        "form_id": "d15cd168-4001-4f7e-8e59-d66eb9524a37",
        "to_status": "published"
      },
      "target_url": "https://your-site.example.com/hooks/4f29c329-8f19-419c-ad0a-519232d73ee8",
      "user_id": "1c2e2e9b-529a-4870-8781-311e83ab95a1",
      "created_at": "2021-01-28T13:16:39.917Z"
    }
  ]
}
```

This endpoint retrieves all webhook subscriptions for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/webhook_subscriptions`

## Create A Webhook Subscriptions

> Request

```
POST http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/webhook_subscriptions
```

```json
{
  "event_name": "response.status_changed",
  "target_url": "https://your-site.example.com/hooks/4f29c329-8f19-419c-ad0a-519232d73ee8",
  "filters": {
    "form_id": "d15cd168-4001-4f7e-8e59-d66eb9524a37",
    "to_status": "published"
  }
}
```

> Response

```json
{
  "data": {
    "id": "cb836066-c343-4b0a-8516-dbd802567b92",
    "event_name": "response.status_changed",
    "filters": {
      "form_id": "d15cd168-4001-4f7e-8e59-d66eb9524a37",
      "to_status": "published"
    },
    "target_url": "https://your-site.example.com/hooks/4f29c329-8f19-419c-ad0a-519232d73ee8",
    "user_id": "1c2e2e9b-529a-4870-8781-311e83ab95a1",
    "created_at": "2021-01-28T13:16:39.917Z"
  }
}
```

This endpoint creates a webhook subscription for a specific event. Additional `filters` can be provided.

### HTTP Request

`POST http://api.boast.io/v1/accounts/{account_id}/webhook_subscriptions`

### Parameters

| Name         | Notes                                                                                                            |
| ------------ | ---------------------------------------------------------------------------------------------------------------- |
| `event_name` | **Required** <br /> See table of possible events below.                                                          |
| `target_url` | **Required**                                                                                                     |
| `filters`    | Optional object of filters checked when sending webhook requests. See table of supported filters by event below. |

### Webhook Events

| Name                     | Supported Filters   |
| ------------------------ | ------------------- |
| `response.available`     | `form_id`           |
| `response.status_change` | `form_id`, `status` |
| `response.published`     | `form_id`           |
| `response.destroyed`     | `form_id`           |
| `contact.created`        |                     |
| `contact.updated`        |                     |
| `contact.destroyed`      |                     |

## Destroy a Webhook Subscription

> Request

```
DELETE http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/webhook_subscriptions/cb836066-c343-4b0a-8516-dbd802567b92
```

> Response

```
204 No Content
```

This endpoint destroys a webhook subscription.

### HTTP Request

`DELETE http://api.boast.io/v1/accounts/{account_id}/webhook_subscriptions/{webhook_subscription_id}`
