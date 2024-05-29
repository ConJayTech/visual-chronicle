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
| `release_year` | string | The movie's release year |
| `director` | string | The movie's director |
