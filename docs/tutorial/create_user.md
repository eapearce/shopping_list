---
layout: page
---

# Tutorial: Creating a user

Follow this tutorial to create a user. You must create a user before you can add a product. Expect this tutorial to take about 10 minutes to complete.

 **Note:** Parameter values are case sensitive.

## Before you begin

Set up your system and start your local service before you begin.

## Postman

After you have started the service, complete the following steps to create a user by using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Select **POST** in the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/users`.
4. In the **Headers** tab, specify the **Key** as `Content-Type` and the **Value** as `application/json`.
5. Create the request body with the following properties:

    * `lastName`
    * `firstName`
    * `email`

    **Example POST request**

    ```json
    {
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com"
    }
      ```

6. Click **Send**.

    **Result:** The system responds with a `201` message and the entry created, which contains the `id` parameter.

    **Example successful response**

    ```json
    {
        "id": "f411",
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com"
    }
    ```
