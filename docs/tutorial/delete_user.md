---
layout: page
---

# Tutorial: Deleting a user

Follow this tutorial to delete a user. Expect this tutorial to take about 10 minutes to complete.

## Before you begin

Set up your system and start your local service before you begin.

## Postman

After you have started the service, complete the following steps to create a product using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Select **DELETE** in the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/users/{id}` where `id` is the `id` of the entry you wish to change.
4. Click **Send**.

    **Result:** The service responds with a `200` message and a record of the deleted object.

    **Example `DELETE` response**

    ```json
     {
        "id": "f411",
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com"
    }
    ```
