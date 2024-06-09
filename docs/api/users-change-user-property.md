---
layout: page
---

# Update user properties

The Patch request updates either one specified property or multiple in the [`user`](user) object.

**Note** : *After creating a user, a unique identifier (ID) is assigned. Provide the ID for the user in the REST URL.*

## URL

```shell
{server_url}/users/{id}
```

## Method

PATCH

## Params

This table lists the properties that can be updated.

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `name` | string | The user's new name that will replace the name in the current record |
| `email` | string | The user's new last email |

## Request headers

Content-Type: application/json

## Sample request body

This example updates the user's email address and name.

```json
[
    {
        "name": "Jake Pots",
        "email": "jpots@example.com",
    }
]
```

## Sample return body

This return shows the updated user record with a new email address.

```json
[
    {
        "name": "Jake Pots",
        "email": "jpots@example.com",
        "id": 3
    }
]
```


## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Removes the user and returns an empty response. |
| 404 | Error | Specified user record not found. |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Request example (shell)

```shell
curl --location --request PATCH 'localhost:3000/users/3' \
--header 'Content-Type: application/json' \
--data-raw '    {
        "name": "Jake Pots",
        "email": "jpots@example.com",
    }'
```
