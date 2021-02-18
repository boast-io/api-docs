# Authentication (OAuth 2)

The Boast API uses the [OAuth 2](https://www.oauth.com/) protocol for authentication, specifically the [Authorization Code Grant](https://oauth.net/2/grant-types/authorization-code/).

## Creating an Application

If you're building a custom integration with Boast and need OAuth access, please [contact us](https://boast.io/contact) to request access.

## Authorize

> Request

```
GET https://app.boast.io/oauth/authorize?client_id=mBUYVNhbzejU9mi4faMzwFE27XunvbKfpf-1jLJfylc&redirect_uri=https://oauthdebugger.com/debug&scope=read write&response_type=code
```

> Redirect

```
GET https://oauthdebugger.com/debug?code=axoIQaYBbm0ZEoj-sZEs-kslTxtR1hJzv4CXsEL3Z_E
```

`GET https://app.boast.io/oauth/authorize`

<aside class="notice">
Authentication end points use <code>app.boast.io</code> host while all other API end points use <code>api.boast.io</code> host.
</aside>

### Query Parameters

| Name          |
| ------------- |
| client_id     |
| redirect_uri  |
| scope         |
| response_type |

## Access Token

> Request

```
> POST https://app.boast.io/oauth/token
> content-type: application/x-www-form-urlencoded

grant_type=authorization_code&
code=axoIQaYBbm0ZEoj-sZEs-kslTxtR1hJzv4CXsEL3Z_E&
client_id=mBUYVNhbzejU9mi4faMzwFE27XunvbKfpf-1jLJfylc&
client_secret=jsockwdoddKjDYUgxrPYGodyOxu3HjI5HaG0C-guDhE&
redirect_uri=https%3A%2F%2Foauthdebugger.com%2Fdebug
```

> Response

```json
{
  "access_token": "MNgOvnS_wcg4h-b5WxTAuof6-K4LgfW9G45543hzmaI",
  "token_type": "Bearer",
  "expires_in": 7200,
  "refresh_token": "a9kSGp7uYsgNIZQAdxN_HJ8Sto_9ASh4-uawGIWZ9Z4",
  "scope": "read write",
  "created_at": 1613653883
}
```

`POST https://app.boast.io/oauth/token`

<aside class="notice">
Authentication end points use <code>app.boast.io</code> host while all other API end points use <code>api.boast.io</code> host.
</aside>

### Parameters

| Name          |                              |
| ------------- | ---------------------------- |
| grant_type    | `authorization_code`         |
| code          | Code from authorize redirect |
| client_id     |                              |
| client_secret |                              |
| redirect_uri  |                              |

## Refresh Token

> Request

```
> POST https://app.boast.io/oauth/token
> content-type: application/x-www-form-urlencoded

grant_type=refresh_token&
refresh_token=a9kSGp7uYsgNIZQAdxN_HJ8Sto_9ASh4-uawGIWZ9Z4&
client_id=mBUYVNhbzejU9mi4faMzwFE27XunvbKfpf-1jLJfylc&
client_secret=jsockwdoddKjDYUgxrPYGodyOxu3HjI5HaG0C-guDhE
```

> Response

```json
{
  "access_token": "YO1JwYRXyOdT4cOxCn5rWLXnXNRDbcRxfXxcszUGMzE",
  "token_type": "Bearer",
  "expires_in": 7200,
  "refresh_token": "8fKtyDtzyChjuNZ3hoFvSpD1wGpZpKeUkFcLe-tR6zA",
  "scope": "read write",
  "created_at": 1613654860
}
```

`POST https://app.boast.io/oauth/token`

<aside class="notice">
Authentication end points use <code>app.boast.io</code> host while all other API end points use <code>api.boast.io</code> host.
</aside>

### Parameters

| Name          |                              |
| ------------- | ---------------------------- |
| grant_type    | `refresh_token`              |
| refresh_token | Token from last access token |
| client_id     |                              |
| client_secret |                              |
