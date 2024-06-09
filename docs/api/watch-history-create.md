---
layout: page
---

# Create watch history

Creates a [`watch history`](watch-history) object in Visual Chronicle.
The request body contains the new movie details.
You must specify the required properties for the movie.

## URL

```shell
POST {server_url}/watchHistory/
```

## Request headers

Content-Type: application/json

## Request body

In the request body, specify a JSON representation of the [`watch history`](watch-history) object. The following table lists the properties that are required when you create a movie.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | number | The ID of the user resource to which this watch history is assigned |
| `movie_id` | string | The ID of the movie resource to which this watch history is assigned |
| `watched_date` | string | The date the user watched the movie |
| `location` | string | The location/format/service where the movie was watched |

## Sample request

The POST body should look something like this. You can change the values of each property as you’d like.

```js
[
    {
      "user_id": 1,
      "movie_id": 1,
      "watched_date": "2024-05-20",
      "location": "theater",
    }
]
```

## Return body

The following example shows the response. Note that the names should be the same as you used in your **Request body** and the response should include the new movie’s id. The movie’s id is automatically generated when the movie is created.

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
| 201 | Created | movie data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
