---
layout: page
---
# `watch-history` resource

Base endpoint:

```shell
{server_url}/watchHistory
```

Contains information about the watch history logged in the watch history of the service.

To have a watch history in the service, a user must be added to the service first.

## Resource Properties

Sample `watch-history` resource

```js
{
    "user_id": 1,
    "movie_id": 1,
    "watched_date": "2024-05-20",
    "location": "theater"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | number | The ID of the user resource to which this watch history is assigned |
| `movie_id` | string | The ID of the movie resource to which this watch history is assigned |
| `watched_date` | string | The date the user watched the movie |
| `location` | string | The location/format/service where the movie was watched |

## Operations

The `watch-history` resource supports these operations.

### READ (GET)

* [Get all watch history](watch-history-get-all)
* [Get watch history by user ID](watch-history-get-by-user-id)
* [Get watch history by movie ID](watch-history-get-by-movie-id)
* [Get watch history by watched date](watch-history-get-by-date)
* [Get watch history by location](watch-history-get-by-location)

### CREATE (POST)

* [Create watch history](watch-history-create)

### DELETE

* [Delete watch history by ID](watch-history-delete-by-id)
