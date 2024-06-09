---
layout: page
---
# Get all watch history

Returns an array of [`watch history`](watch history) objects that contains all users that have registered with the service.

## URL

```shell
{server_url}/watchHistory
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
      "user_id": 1,
      "movie_id": 1,
      "watched_date": "2024-05-20",
      "location": "theater",
      "id": "105c"
    },
    {
      "user_id": 1,
      "movie_id": 2,
      "watched_date": "2024-05-22",
      "location": "streaming",
      "platform": "Netflix",
      "id": "991a"
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
