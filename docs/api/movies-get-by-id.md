---
layout: page
---

# Get movie by ID

Returns an array of  [`movie`](movies) objects that contains only the movies specified by the `id` parameter, if it exists.

## URL

```shell
{server_url}/movies/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the movies to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "id": 3,
      "title": "Interstellar",
      "release_year": 2014,
      "director": "Christopher Nolan"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified movies record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
