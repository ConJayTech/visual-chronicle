---
layout: page
---

# Get watch history by date watched

Returns an array of  [`watch history`](watch-history) objects that contains only the watch history specified by the `watched_date` parameter, if it exists.

## URL

```shell
{server_url}/watchHistory?watched_date=<watched_date_to_search_for>
```

## Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `watched_date` | string | The date the user watched the movie |

## Request headers

None

## Request body

None

## Return body

```js
[
     {
      "user_id": 2,
      "movie_id": 1,
      "watched_date": "2024-05-24",
      "location": "physical_media",
      "media_type": "Blu-ray",
      "id": "7ba0"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified watch history record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
