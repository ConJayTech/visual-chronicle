---
layout: page
---

# Delete watch history by ID

Removes the `watch history` you identify in the `id` parameter from the watch history resource, if the watch history exists.

## URL

```shell
{server_url}/watchHistory?id=<id_to_delete>
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `id` | string | The record ID of the watch history to delete |

## Request headers

Content-Type: application/json

## Request body

```shell
DELETE {server_url}/watchHistory?id=<id_to_delete>
```

## Return body

Returns the watch history you deleted from the watch history resource

```js
[
    {
      "user_id": 1,
      "movie_id": 1,
      "watched_date": "2024-05-20",
      "location": "theater",
      "id": "105c"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Action completed successfully |
| 202 | Accepted| Action has been queued |
| 204 | No Content| Action has been performed, but the response does not include an entity |
| 404 | Error | Specified watch history record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related topics

[Create a new watch history](watch-history-create)
