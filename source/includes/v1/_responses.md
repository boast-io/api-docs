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
      "photo": {
        "original_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/b7e9178d-acf3-4d29-afe0-b53624a02392/photos/6bd306ed-ec26-49fb-9bca-bcc3f216b0fe/original-184fb12980f96efb2ff88ea8b67a7a42.jpg",
        "large_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/b7e9178d-acf3-4d29-afe0-b53624a02392/photos/6bd306ed-ec26-49fb-9bca-bcc3f216b0fe/large-c5cba0f17e3f208062e164a28ff46163.jpg",
        "medium_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/b7e9178d-acf3-4d29-afe0-b53624a02392/photos/6bd306ed-ec26-49fb-9bca-bcc3f216b0fe/medium-d0199a3f7d97bd6bc007a949c8709148.jpg"
      },
      "video": {
        "original_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/original-5968437c107cca65646ec23ea7d35741.webm",
        "mp4_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/video_mp4-d0199a3f7d97bd6bc007a949c8709148.mp4",
        "webm_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/video_webm-862dafe4680cf32d6c9b7d6af04d810a.webm",
        "thumbnail_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/thumbnails-d5a91ed5d66fd98ec430fbff7b01c534-1.jpg"
      },
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
