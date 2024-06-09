---
layout: page
---
# Get all movies

Returns an array of [`movie`](movies) objects that contains all users that have registered with the service.

## URL

```shell
{server_url}/movies
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
      "id": 1,
      "title": "Inception",
      "release_year": 2010,
      "director": "Christopher Nolan"
    },
    {
      "id": 2,
      "title": "The Matrix",
      "release_year": 1999,
      "director": "Lana Wachowski, Lilly Wachowski"
    }
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
