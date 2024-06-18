---
layout: page
---

# First-Use: Enroll a new user

In this tutorial, you will enroll a new user, Jack, in the Visual Chronicle service so he can be assigned a new [`watch history`](../api/watch-history).

Expect this tutorial to take about 15 minutes to complete.

## Enroll a new user

You will enroll Jack using Postman, a user-friendly API client. Postman will allow you to easily `POST` a new [`user`](../api/user) resource containing the user's details.

To enroll a new user:

1. First confirm our local service is running in the command window with the following:

    ```shell
    cd <your-github-workspace>/visual-chronicle/api
    # Run the service and monitor its database file for updates
    json-server database.json
    ```

1. Next, open the Postman app on your desktop.
1. In the Postman app, create a new request and input these values:
    * **METHOD**: POST
    * **URL**: `{base_url}/users`
        * `{base_url}` may depends on installation, but is typically `http://localhost:3000`
    * **Headers**: `Content-Type: application/json`
    * **Request body**: `raw`

        | Property | Description | Type | Required | Notes |
        | -------------- | ------ | ------------ |------------ |------------ |
        | name | The user's name. | string | Required |   |
        | email | The user's email. | string | Required | A unique email is required. |

        In the Request Body, the JSON script of those properties will be entered like this:

        ```js
        {
            "name": "Jack Wilson",
            "email": "jack.wilson@example.com"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

    ```js
    {
        "name": "Jack Wilson",
        "email": "jack.wilson@example.com"
        "id": 5
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to make REST API calls.
