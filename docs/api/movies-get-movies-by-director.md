---
layout: page
---

# Get movie by director

Returns an array of  [`movie`](movie) objects that contains only the movie specified by the `director` query parameter, if it exists.

## URL

```shell
{server_url}/movies/?director=<director_to_find>
```

## Query Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `director` | string | The director  of the movie to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "id": 5,
      "title": "Pulp Fiction",
      "release_year": 1994,
      "director": "Quentin Tarantino"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified movie record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
