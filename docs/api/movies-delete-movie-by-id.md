---
layout: page
---

# Delete movie by ID

Removes the movie you identify in the `id` parameter from the movie resource, if the movie exists.

## URL

```shell
{server_url}/movies/{id}
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | number | The record ID of the movie to delete |

## Request headers

Content-Type: application/json

## Request body

```shell
DELETE {server_url}/movies/{id}
```

## Return body

Returns the movie you deleted from the movie resource

```js
[
    {
      "id": 7,
      "title": "Fight Club",
      "release_year": 1999,
      "director": "David Fincher"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified movie record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related topics

[Create a new movie](movies-create-movie)
