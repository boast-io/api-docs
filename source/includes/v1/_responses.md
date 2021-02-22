# Responses

## Get All Responses

> Request

```
GET http://api.boast.io/v1/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/responses
```

> Response

```json
{
  "data": [
    {
      "id": "d33c2315-f15f-4679-8ecb-e1f546f33eb0",
      "form_id": "b345d73d-197c-4990-8a0c-ee5f58287f98",
      "contact_id": "a308c983-dea1-4e73-9f4c-89db9c22cff0",
      "location_id": "3e340197-e579-40e1-8ed0-05a78aa26ece",
      "staff_id": "a17a4c54-6df6-48f1-aff3-f68a4aedcd7d",
      "consent": "not_applicable",
      "rating_type": "five_stars",
      "rating": 5,
      "rating_max": 5,
      "sentiment": "promoters",
      "feedback": "Her?",
      "headline": "Solid as a Rock!",
      "first_name": "Michael",
      "last_name": "Bluth",
      "email": "michael.bluth@example.com",
      "mobile_phone": "555-555-5555",
      "company": "Bluth Company",
      "job_title": "President",
      "photo_url": "https://assets.boast.io/app/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/responses/d33c2315-f15f-4679-8ecb-e1f546f33eb0/photos/e744b1a8-3b0f-4cf9-9583-d51dec75c1fa/original-779db8f190a1901824bd32f80b376d47.png",
      "video_url": "https://assets.boast.io/app/accounts/7a2f1f8c-7771-47e2-8dbd-332b301028a8/responses/d33c2315-f15f-4679-8ecb-e1f546f33eb0/videos/c4e033de-ac70-4f4e-b4ef-598dc152697a/original-20fde3bc63182beddb0e29db7967439b.webm",
      "additional_fields": {
        "my_custom_field": "Hello World!"
      },
      "status": "needs_review",
      "weight": 1,
      "accepted": "2021-02-11T17:47:52.940Z",
      "created": "2021-02-11T15:13:41.784Z",
      "updated": "2021-02-11T17:49:32.164Z"
    }
  ]
}
```

This endpoint retrieves all responses for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/responses`
