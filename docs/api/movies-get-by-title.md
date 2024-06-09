---
layout: page
---

# Get movies by  name

Returns an array of  [`movie`](movies) objects that contains only the movies specified by the `title` parameter, if it exists.

## URL

```shell
{server_url}/movies?title=<title to find>
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `title` | string | The title of the movies to return |

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
| 404 | Error | Specified property not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
