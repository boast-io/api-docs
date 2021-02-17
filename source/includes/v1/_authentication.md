# Authentication (OAuth 2)

The Boast API uses the [OAuth 2](https://www.oauth.com/) protocol for authentication, specifically the [Authorization Code Grant](https://oauth.net/2/grant-types/authorization-code/).

## Creating an Application

If you're building a custom integration with Boast and need OAuth access, please [contact us](https://boast.io/contact) to request access.

## Authorize

```
GET https://app.boast.io/oauth/authorize?client_id=mBUYVNhbzejU9mi4faMzwFE27XunvbKfpf-1jLJfylc&redirect_uri=https://oauthdebugger.com/debug&scope=read write&response_type=code
```

`GET https://app.boast.io/oauth/authorize`

### Query Parameters

| Name          |
| ------------- |
| client_id     |
| redirect_uri  |
| scope         |
| response_type |

## Access Token

```
POST https://app.boast.io/oauth/token
```

```json
{
  "grant_type": "authorization_code",
  "code": "nuQL_bzE9zQowsVTnfnN9mjBqNCwLrDDeoFoBkefdiw",
  "client_id": "mBUYVNhbzejU9mi4faMzwFE27XunvbKfpf-1jLJfylc",
  "client_secret": "{clientSecret}",
  "redirect_uri": "https://oauthdebugger.com/debug"
}
```

`POST https://app.boast.io/oauth/token`

### Parameters

| Name          |
| ------------- |
| grant_type    |
| code          |
| client_id     |
| client_secret |
| redirect_uri  |

## Refresh Token

`POST https://app.boast.io/oauth/token`

### Parameters

| Name          |
| ------------- |
| refresh_token |
| grant_type    |
