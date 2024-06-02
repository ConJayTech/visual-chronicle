---
layout: page
---
# `watch-history` resource

Base endpoint:

```shell
{server_url}/watch-history
```

Contains information about the movies logged in the watch history of the service.

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
