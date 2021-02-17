# Sequence Enrollments

## Get All Sequence Enrollments

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/sequence_enrollments
```

> Response

```json
{
  "data": [
    {
      "id": "09f1bd66-84fe-454f-ac12-4dc323f656aa",
      "contact_id": "61a06314-fa2e-4fc8-bbcf-f942075042cc",
      "sequence_id": "df51783e-c81c-460b-82dc-8c5a63b70e92",
      "response_id": "ee456cc9-91a9-48c2-8f04-4e28d92788d2",
      "status": "completed",
      "created_at": "2021-02-04T21:13:44.005Z",
      "updated_at": "2021-02-04T21:13:44.005Z"
    }
  ]
}
```

This endpoint retrieves all sequence enrollments for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/sequence_enrollments`

## Get a Specific Sequence Enrollment

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/sequence_enrollments/09f1bd66-84fe-454f-ac12-4dc323f656aa
```

> Response

```json
{
  "data": {
    "id": "09f1bd66-84fe-454f-ac12-4dc323f656aa",
    "contact_id": "61a06314-fa2e-4fc8-bbcf-f942075042cc",
    "sequence_id": "df51783e-c81c-460b-82dc-8c5a63b70e92",
    "response_id": "ee456cc9-91a9-48c2-8f04-4e28d92788d2",
    "status": "completed",
    "created_at": "2021-02-04T21:13:44.005Z",
    "updated_at": "2021-02-04T21:13:44.005Z"
  }
}
```

This endpoint retrieves a single sequence enrollment.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/sequence_enrollments/{enrollment_id}`

## Create A Sequence Enrollment

> Request

```
POST http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/sequence_enrollments
```

```json
{
  "contact_id": "6d1c8d94-c598-461e-ad76-f4851e4af9d4",
  "sequence_id": "e16f6028-cfc1-4d9d-a087-0a8574d2f13f"
}
```

> Response

```json
{
  "data": {
    "id": "09f1bd66-84fe-454f-ac12-4dc323f656aa",
    "contact_id": "6d1c8d94-c598-461e-ad76-f4851e4af9d4",
    "sequence_id": "e16f6028-cfc1-4d9d-a087-0a8574d2f13f",
    "response_id": null,
    "status": "active",
    "created_at": "2021-02-04T21:13:44.005Z",
    "updated_at": "2021-02-04T21:13:44.005Z"
  }
}
```

This endpoint enrolls an existing contact in a sequence.

### HTTP Request

`POST http://api.boast.io/v1/accounts/{account_id}/sequence_enrollments`

### Parameters

| Name          | Notes        |
| ------------- | ------------ |
| `contact_id`  | **Required** |
| `sequence_id` | **Required** |

## Remove a Sequence Enrollment

> Request

```
DELETE http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/sequence_enrollments/09f1bd66-84fe-454f-ac12-4dc323f656aa
```

> Response

```json
{
  "data": {
    "id": "09f1bd66-84fe-454f-ac12-4dc323f656aa",
    "contact_id": "61a06314-fa2e-4fc8-bbcf-f942075042cc",
    "sequence_id": "df51783e-c81c-460b-82dc-8c5a63b70e92",
    "response_id": "ee456cc9-91a9-48c2-8f04-4e28d92788d2",
    "status": "removed",
    "created_at": "2021-02-04T21:13:44.005Z",
    "updated_at": "2021-02-04T21:13:44.005Z"
  }
}
```

This endpoint unenrolls a contact with an active enrollment from a sequence.

### HTTP Request

`DELETE http://api.boast.io/v1/accounts/{account_id}/sequence_enrollments/{enrollment_id}`
