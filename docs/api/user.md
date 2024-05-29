---
layout: page
---
# `user` resource

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the service.

To have a watch history in the service, the user must be registered to the service first.

## Resource Properties

Sample `user` resource

```js
{
    "id": 1,
    "name": "Alice Johnson",
    "email": "alice@example.com"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The user's unique record ID |
| `name` | string | The user's name |
| `email` | string | The user's email address |

## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get users by ID](users-get-user-by-id)
* [Get users by Email](users-get-user-by-email)
* [Get users by names](users-get-users-first-names)

### CREATE (POST)

* [Create user](users-create-user)

### UPDATE (PUT/PATCH)

* [Update user by ID](users-update-by-id)
* [Change user email](users-change-user-email.md)
* [Change user property](users-change-user-property)

### DELETE

* [Delete user by ID](users-delete-user-by-id)
