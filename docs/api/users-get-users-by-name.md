---
layout: page
---

# Get user by  name

Returns an array of  [`user`](user) objects that contains only the user specified by the `name` parameter, if it exists.

## URL

```shell
{server_url}/users?name=<name to find>
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `name` | string | The name of the user to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "id": 4,
      "name": "David Brown",
      "email": "david@example.com"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified property not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
