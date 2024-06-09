---
layout: page
---

# Create movie

Creates a [`movie`](movie) object in Visual Chronicle.
The request body contains the new movie details.
You must specify the required properties for the movie.

## URL

```shell
POST {server_url}/movies/
```

## Request headers

Content-Type: application/json

## Request body

In the request body, specify a JSON representation of the [`movie`](movie) object. The following table lists the properties that are required when you create a movie.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The movie's name |
| `release_year` | string | The movie's release year |
| `director` | string | The movie's director |

## Sample request

The POST body should look something like this. You can change the values of each property as you’d like.

```js
[
    {
      "title": "The Godfather",
      "release_year": 1972,
      "director": "Francis Ford Coppola"
    }
]
```

## Return body

The following example shows the response. Note that the names should be the same as you used in your **Request body** and the response should include the new movie’s id. The movie’s id is automatically generated when the movie is created.

```js
[
    {
      "id": 6,
      "title": "The Godfather",
      "release_year": 1972,
      "director": "Francis Ford Coppola"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | movie data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
