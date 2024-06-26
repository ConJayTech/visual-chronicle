---
layout: page
---

# Get user by Email

Returns an array of  [`user`](user) objects that contains only the user specified by the `email` query parameter, if it exists.

## URL

```shell
{server_url}/users/?email=<email_address_to_find>
```

## Query Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `email` | string | The email address of the user to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "id": 1,
      "name": "Alice Johnson",
      "email": "alice@example.com"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified user record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
