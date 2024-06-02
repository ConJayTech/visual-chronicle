---
layout: page
---

# Tutorial: Enroll a new user

In this tutorial, you learn the operations to call to
enroll a new user into the service.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start) topic on the development system you'll use for the tutorial.

## Enroll a new user

You can enroll a new user in Visual Chronicle. To do so, `POST` a new [`user`](../api/user) resource containing the user's details.

To enroll a new user:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/visual-chronicle/api
    # Run the service and monitor its database file for updates
    json-server database.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/users`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**: `raw`

        You can change the values of each property as you'd like.

        ```js
        {
            "name": "Jimmy Jones",
            "email": "jjones@example.com"
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the names should be the same as you used in your **Request body** and the response should include the new user's `id`.

    ```js
    {
        "name": "Jimmy Jones",
        "email": "jjones@example.com",
        "id": "5eof"
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
