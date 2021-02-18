# Interacting with the API

Unless otherwise noted, all API requests and responses utilize the `JSON` data format.
Some API endpoints may support URI parameters in the query string.

## Requests

> Example Request Headers

```
Authorization: Bearer {token}
Content-Type: application/json
```

> Example Request Body

```json
{
  "first_name": "Michael",
  "last_name": "Bluth"
}
```

Unless otherwise noted, all API requests should:

- include the `Authorization` header with a `Bearer` token value (see Authentication above)
- set the `Content-Type: application/json` header
- use the `JSON` format for the request body

## Responses

> Example Response Headers

```
Content-Type: application/json
```

> Example Response Body (multiple objects returned)

```json
{
  "data": [
    {
      "first_name": "Michael",
      "last_name": "Bluth"
    },
    {
      "first_name": "Lucille",
      "last_name": "Ball"
    }
  ]
}
```

> Example Response Body (single object returned)

```json
{
  "data": {
    "first_name": "Michael",
    "last_name": "Bluth"
  }
}
```

Unless otherwise noted, all API responses use the `JSON` format.

Data for the response is returned under a top-level `data` key, which is either an `array[]` of data objects, or a single data object.

## Errors

```
HTTP/1.1 400 Bad Request
```

```json
{
  "errors": [
    {
      "detail": "A detailed error message",
      "code": "bad_request",
      "status": 400
    }
  ]
}
```

Boast utilizes standard [HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) to indicate the status of an API request.

In general, anything in the `2xx` range should be considered successful, and anything in the `4xx` or `5xx` range should be considered an error.

Some API endpoints will provide additional error objects inside a top-level `errors` key of the `JSON` response.

### Error Objects

| Key      | Notes                                                              |
| -------- | ------------------------------------------------------------------ |
| `detail` | Human friendly description of the error                            |
| `code`   | Internal error code, expressed as a string                         |
| `status` | _Optional_ HTTP status code related to the error                   |
| `source` | _Optional_ Object containing references to the source of the error |

## Pagination

> Example Pagination Response

```json
{
  "data": [
    {
      "first_name": "Michael",
      "last_name": "Bluth"
    },
    {
      "first_name": "Lucille",
      "last_name": "Ball"
    },
    {
      "first_name": "Tony",
      "last_name": "Hawk"
    }
  ],
  "meta": {
    "pagination": {
      "count": 103,
      "page": 1,
      "items": 3,
      "pages": 35
    }
  }
}
```

Some API endpoints may return paginated results inside a `pagination` object underneath a top-level `meta` key in the response. The current page is set with the `page` query parameter.

### Pagination Object

| Key     | Notes                    |
| ------- | ------------------------ |
| `count` | Total count of items     |
| `page`  | Current page number      |
| `items` | Number of items per page |
| `pages` | Number of total pages    |
