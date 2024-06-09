---
layout: page
---

# Tutorial: Add a new movie

In this tutorial, you learn the operations to add a new movie into the service.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

Make sure you've completed the [Before you start a tutorial](before-you-start) topic on the development system you'll use for the tutorial.

## Add a new movie

You can add a new movie in Visual Chronicle. To do so, `POST` a new [`movie`](../api/movies) resource containing the movie's details.

To add a new movie:

1. If your local service is not running, start it.

    ```shell
    cd <your-github-workspace>/visual-chronicle/api
    # Run the service and monitor its database file for updates
    json-server database.json
    ```

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request with these values:
    * **METHOD**: POST
    * **URL**: `{{base_url}}/movies`
    * **Headers**: `Content-Type: application/json`
    * **Request body**: `raw`

        You can change the values of each property as you'd like.

        ```js
        {
            "title": "Forrest Gump",
            "release_year": 1994,
            "director": "Robert Zemeckis"
        }    
        ```

1. In the Postman app, choose **Send** to make the request.
1. Watch for the response body, which should look something like this. Note that the property values should be the same as you used in your **Request body** and the response should include the new movie's `id`.

    ```js
    {
        "id": 9
        "title": "Forrest Gump",
        "release_year": 1994,
        "director": "Robert Zemeckis"
    }  
    ```

After doing this tutorial in Postman, you might like to repeat it in
your favorite programming language. To do this, adapt the values from
the tutorial to the properties and arguments that the language uses to
make REST API calls.

## Next steps

[Add a watch history to the service](tutorial-add-watch-history)
