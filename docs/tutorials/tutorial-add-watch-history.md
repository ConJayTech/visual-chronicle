---
layout: page
---

# Tutorial: Post a new watch history

In this tutorial, you learn the operations to post a new watch history into the service.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start) topic on the development system you'll use for the tutorial.

## post a new watch history

You can post a new watch history in Visual Chronicle. To do so, `POST` a new [`watch history`](../api/watch-history) resource containing the watch history's details.

To post a new watch history:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/visual-chronicle/api
    # Run the service and monitor its database file for updates
    json-server database.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/watchHistory`
    * **Headers**: `Content-Type: application/json`
    * **Request body**: `raw`

        You can change the values of each property as you'd like.

        Each watch history must be assigned a `user` ("user_id") and a `movie` ("movie_id").

        ```js
        {
            "user_id": 4,
            "movie_id": 6,
            "watched_date": "2024-05-28",
            "location": "streaming",
            "platform": "Hulu",
        }
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the property values should be the same as you used in your **Request body** and the response should include the new watch history's `id`.

    ```js
    {
        "user_id": 4,
        "movie_id": 6,
        "watched_date": "2024-05-28",
        "location": "streaming",
        "platform": "Hulu",
        "id": "ae10"
    }
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.
