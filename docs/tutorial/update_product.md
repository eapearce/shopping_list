---
layout: page
---

# Tutorial: Update a product

Follow this tutorial to change a product parameter. You can change any of the following parameters.

* `UserId`
* `productName`
* `storeName`
* `lastPurchased`
* `intervalMonths`

 Expect this tutorial to take about 10 minutes to complete.

 **Note:** Parameter values are case sensitive.

## Before you begin

Set up your system and start your local service before you begin.

## Postman

After you have started the service, complete the following steps to create a product using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Select **PATCH** in the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/products/{id}` where `id` is the `id` of the entry you wish to change.
4. In the **Headers** tab, specify the **Key** as `Content-Type` and the **Value** as `application/json`.
5. Create the request body with the parameter you want to replace:

    **Example PATCH request**

    ```json
    { 
        "storeName": "King Soopers",
    }
    ```

6. Click **Send**.

    **Result:** The system responds with a `200` message and the entry created, which contains the `id` parameter.

    **Example PATCH request**

    ```json
   {
        "storeName": "King Soopers",
        "id": "1"
    }
    ```
