---
layout: page
---
# Get all users

Returns an array of [`user`](user) objects that contains all users that have registered with the service.

## URL

```shell
{server_url}/users
```

## Params

None

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
    },
    {
      "id": 2,
      "name": "Bob Smith",
      "email": "bob@example.com"
    },
    {
      "id": 3,
      "name": "Carol White",
      "email": "carol@example.com"
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
