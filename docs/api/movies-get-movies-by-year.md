---
layout: page
---

# Get movie by release year

Returns an array of  [`movie`](movie) objects that contains only the movie specified by the `release year` query parameter, if it exists.

## URL

```shell
{server_url}/movies/?release_year=<release_year_to_find>
```

## Query Params

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `release year` | string | The release year address of the movie to return |

## Request headers

None

## Request body

None

## Return body

```js
[
    {
      "id": 4,
      "title": "The Shawshank Redemption",
      "release_year": 1994,
      "director": "Frank Darabont"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified movie record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
