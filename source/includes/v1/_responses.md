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
      "id": "174de834-eb54-4e33-9d87-4d104239894e",
      "status": "published",
      "thumbnail": {
        "url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/c58aa5f8-3210-4a2a-b3ca-3a469bf2b424/teaser-35f98ba2c93ac7407625a23d8f954837.jpg",
        "open_graph_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/c58aa5f8-3210-4a2a-b3ca-3a469bf2b424/open_graph-b1a53d08c5c359511b7f07222e6dc960.jpg",
        "unprocessed_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/c58aa5f8-3210-4a2a-b3ca-3a469bf2b424/original-0ab2ebccb2daac4b8194ab2499c504dc.png"
      },
      "consent": "received",
      "display_weight": 1,
      "form_id": "b345d73d-197c-4990-8a0c-ee5f58287f98",
      "contact_id": "a308c983-dea1-4e73-9f4c-89db9c22cff0",
      "location_id": "3e340197-e579-40e1-8ed0-05a78aa26ece",
      "staff_id": "a17a4c54-6df6-48f1-aff3-f68a4aedcd7d",
      "accepted": "2021-02-11T17:47:52.940Z",
      "created": "2021-02-11T15:13:41.784Z",
      "updated": "2021-02-11T17:49:32.164Z",
      "fields": {
        "first_name": "Matt",
        "last_name": "Hall",
        "email": "help@boast.io",
        "feedback": "We love using Boast to collect videos from our customers, it's been an awesome tool for us!",
        "headline": "Boast is great!",
        "sentiment": "promoters",
        "rating": 5,
        "rating_type": "five_stars",
        "rating_max": 5,
        "video": {
          "url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/video_mp4-d0199a3f7d97bd6bc007a949c8709148.mp4",
          "unprocessed_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/4836ed10-7f81-4c37-9157-1979fdcc3d71/videos/95767ab2-b038-4d14-ad48-321b888474d3/original-5968437c107cca65646ec23ea7d35741.webm"
        },
        "photo": {
          "url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/b7e9178d-acf3-4d29-afe0-b53624a02392/photos/6bd306ed-ec26-49fb-9bca-bcc3f216b0fe/medium-d0199a3f7d97bd6bc007a949c8709148.jpg",
          "unprocessed_url": "https://assets.boast.io/app/accounts/6713be5b-dc41-4af3-890a-9a67f2a4a06f/responses/b7e9178d-acf3-4d29-afe0-b53624a02392/photos/6bd306ed-ec26-49fb-9bca-bcc3f216b0fe/original-184fb12980f96efb2ff88ea8b67a7a42.jpg"
        },
        "company": "Boast",
        "job_title": null,
        "mobile_phone": null
      },
      "additional_fields": {
        "my_custom_field": "Hello World!"
      },
      "tags": [
        {
          "name": "my-tag"
        }
      ],
      "links": {
        "detail": "https://demo.boast.io/responses/174de834-eb54-4e33-9d87-4d104239894e",
        "edit": "https://demo.boast.io/responses/174de834-eb54-4e33-9d87-4d104239894e/edit",
        "share": "https://demo.boast.io/r/174de834-eb54-4e33-9d87-4d104239894e"
      }
    }
  ]
}
```

This endpoint retrieves all responses for an account.

### HTTP Request

`GET http://api.boast.io/v1/accounts/{account_id}/responses`
