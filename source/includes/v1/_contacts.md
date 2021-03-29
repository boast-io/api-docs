# Contacts

## Get All Contacts

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/contacts
```

> Response

```json
{
  "data": [
    {
      "id": "b94f8eb4-6dea-4c25-932d-e25b5954c655",
      "first_name": "Michael",
      "last_name": "Bluth",
      "email": "michael.bluth@example.com",
      "mobile_phone": "+15555555555",
      "organization": "Bluth Company",
      "job_title": "President",
      "time_zone": "Eastern Time (US & Canada)",
      "country_code": "US",
      "location_id": "2f5c4510-65d9-4596-aca7-a4b2bd4918fd",
      "staff_id": "1ec592b5-3d92-43fe-8b3a-3e1f9075fd5e",
      "source": "response",
      "created_at": "2021-02-10T16:54:23.805Z",
      "updated_at": "2021-02-10T16:54:23.805Z",
      "links": {
        "detail": "https://demo.boast.io/contacts/b94f8eb4-6dea-4c25-932d-e25b5954c655",
        "edit": "https://demo.boast.io/contacts/b94f8eb4-6dea-4c25-932d-e25b5954c655/edit"
      }
    }
  ]
}
```

This endpoint retrieves all contacts for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/contacts`

## Create A Contact

> Request

```
POST http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/contacts
```

```json
{
  "email": "george.bluth@example.com",
  "mobile_phone": "+15555555555",
  "first_name": "George",
  "last_name": "Bluth",
  "organization": "Bluth Company",
  "job_title": "President",
  "time_zone": "Eastern Time (US & Canada)",
  "country_code": "US",
  "source": "api"
}
```

> Response

```json
{
  "data": {
    "id": "b94f8eb4-6dea-4c25-932d-e25b5954c655",
    "first_name": "George",
    "last_name": "Bluth",
    "email": "george.bluth@example.com",
    "mobile_phone": "+15555555555",
    "organization": "Bluth Company",
    "job_title": "President",
    "time_zone": "Eastern Time (US & Canada)",
    "country_code": "US",
    "location_id": null,
    "staff_id": null,
    "source": "api",
    "created_at": "2021-02-10T16:54:23.805Z",
    "updated_at": "2021-02-10T16:54:23.805Z",
    "links": {
      "detail": "https://demo.boast.io/contacts/b94f8eb4-6dea-4c25-932d-e25b5954c655",
      "edit": "https://demo.boast.io/contacts/b94f8eb4-6dea-4c25-932d-e25b5954c655/edit"
    }
  }
}
```

This endpoint creates a contact on an account.

### HTTP Request

`POST http://api.boast.io/v1/accounts/{account_id}/contacts`

### Parameters

<aside class="notice">
Either <code>email</code> or <code>mobile_phone</code> is required to create a contact.
</aside>

| Name           | Notes                                                                                                                                          |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `email`        | **Requires** either `email` or `mobile_phone`                                                                                                  |
| `mobile_phone` | **Requires** either `mobile_phone` or `email` <br/> Must be an [E.164](https://www.twilio.com/docs/glossary/what-e164) formatted phone number. |
| `first_name`   |                                                                                                                                                |
| `last_name`    |                                                                                                                                                |
| `organization` |                                                                                                                                                |
| `job_title`    |                                                                                                                                                |
| `time_zone`    |                                                                                                                                                |
| `country_code` | Accepts ISO 3166-1 alpha-2 country code                                                                                                        |
| `source`       | Accepts either `api` or `integration`. If no source is provided, `api` is used                                                                 |
