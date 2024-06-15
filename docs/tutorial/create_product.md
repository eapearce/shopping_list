---
layout: page
---

# Tutorial: Creating a product

Follow this tutorial to create a product. You must create a user before you can add a product. Expect this tutorial to take about 10 minutes to complete.

 **Note:** Parameter values are case sensitive.

## Before you begin

Set up your system and start your local service before you begin.

## Postman

After you have started the service, complete the following steps to create a product using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Select **POST** in the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/products`.
4. In the **Headers** tab, specify the **Key** as `Content-Type` and the **Value** as `application/json`.
5. Create the request body with the following properties:

    * `UserId`
    * `productName`
    * `storeName`
    * `lastPurchased`
    * `intervalMonths`

    **Example POST request**

    ```json
    {
        "userId": 2,
        "productName": "Dog food",
        "storeName": "Amazon",
        "lastPurchased": "2024-04-01",
        "intervalMonths": 1,
    }
    ```

6. Click **Send**.

    **Result:** The system responds with a `201` message and the entry created, which contains the `id` parameter.

    **Example successful response**

    ```json
    {
        "userId": 2,
        "productName": "Dog food",
        "storeName": "Amazon",
        "lastPurchased": "2024-04-01",
        "intervalMonths": 1,
        "id": 10
    }
    ```
