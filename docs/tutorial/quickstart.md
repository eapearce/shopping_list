---
layout: page
---
# Quickstart

Get started with the Recurring Shopping API by completing this set of tutorials. You will set up your system, create your first user, and create your first product. Expect this process to take approximately 30 minutes.

## System set up

Complete the following tutorial to set up your development system.

* System setup [PC](./tutorial/setup_pc.md)
* [MacOS](./tutorial/setup_macos.md)

**Next step:** Create your first user.

## Create a user

Follow this procedure to create your first user via the desktop version of Postman. You must create a user before you can create a product.

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

    **Result:** The system responds with a `201` message and the entry created, which contains the `id` parameter. Take note of the `id` to use when you create a product.

    **Example successful response**

    ```json
    {
        "id": "f411",
        "last_name": "Jones",
        "first_name": "Jenny",
        "email": "jen.jones@example.com"
    }
    ```

**Next step:** Create your first product.

## Create a product

Follow this procedure to create a product using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Select **POST** in the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/products`.
4. In the **Headers** tab, specify the **Key** as `Content-Type` and the **Value** as `application/json`.
5. Create the request body with the following properties. For the `UserId` parameter, specify the `id` of the user you just created.

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

## Next steps

You have now completed the basic tutorials to set up your system and create your first user and product entires.

Like these tutorials? The documentation has [more tutorials](../index.md) for many common use cases.
