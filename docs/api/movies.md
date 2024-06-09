---
layout: page
---
# `movies` resource

Base endpoint:

```shell
{server_url}/movies
```

Contains information about the movies archived in the service.

## Resource Properties

Sample `movie` resource

```js
{
    "id": 1,
    "title": "Inception",
    "release_year": 2010,
    "director": "Christopher Nolan"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The movies's unique record ID |
| `title` | string | The movie's name |
| `release_year` | number | The movie's release year |
| `director` | string | The movie's director |

## Operations

The `movies` resource supports these operations.

### READ (GET)

* [Get all movies](movies-get-all)
* [Get movies by title](movies-get-by-title)
* [Get movies by ID](movies-get-movie-by-id)
* [Get movies by release year](movies-get-movies-by-year)
* [Get movies by director](movies-get-movies-by-director)

### CREATE (POST)

* [Create movie](movies-create-movie)

### DELETE

* [Delete movie by ID](movies-delete-movie-by-id)
