---
layout: page
---

# Create user

Creates a [`user`](user) who is registering with the to-do service.
The request body contains the new user details.
You must specify the required properties for the user.

## URL

```shell

{POST}{server_url}/users/
```

## Request headers

None

## Request body

In the request body, specify a JSON representation of the [`user`](user) object. The following table lists the properties that are required when you create a user.

| Property | Description | Type | Required | Notes |
| -------------- | ------ | ------------ |------------ |------------ |
| name | The user's name | string | Required |  |
| email | The user's email | string | Required | A unique email is required. |

## Sample request

The POST body should look something like this. You can change the values of each property as you’d like.

```js
[
    {
        "name": "Jerry Crawford",
        "email": "jcraw@example.com",
    }
]
```

## Return body

The following example shows the response. Note that the names should be the same as you used in your **Request body** and the response should include the new user’s id. The user’s id is automatically generated when the user is created.

```js
[
    {
        "name": "Jerry Crawford",
        "email": "scough2@uw.edu",
        "id": 9
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 201 | Created | User data created successfully. |
| 500 | Internal server Error | Invalid JSON. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## Related information

* [Handling errors](handling-errors.md)
