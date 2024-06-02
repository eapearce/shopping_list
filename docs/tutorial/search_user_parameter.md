---
layout: page
---

# Tutorial: Search for a user by parameter

You can search for users by any of the following parameters:

* `firstName`
* `lastName`
* `email`
* `id`

The service returns only results that match the search parameters exactly.  **Note:** User names and emails are case sensitive.

Complete this tutorial to learn how to search for a user by the desired parameter.
Expect this tutorial to take about 10 minutes to complete.

## Before you begin

Set up your system and start your local service before you begin.

## Postman

After you have started the service, complete the following steps to search for a user using the desktop version of Postman.

1. In Postman, click the **New** button in Postman and select **HTTP** to create a new request.
2. Ensure **GET** is selected from the dropdown menu next to the request URL.
3. In the URL field, enter the base URL for the Recurring Shopping API, followed by `/users?`, and add the search parameter followed by an equals sign (`=`) and the desired value.
    **Example** `"http://localhost:3000/users?lastName=Powell`
4. Click **Send**.

**Result:** The service returns the all entries that match your criteria. If no user matches the search criteria, the service will return an empty array (`[]`)

#### Example `users` object

```json
[
    {
        "lastName": "Powell",
        "firstName": "Alison",
        "email": "alison.powell@example.com",
        "id": "1"
    }
]
```

## Command line

1. Ensure you have started the service in for your local copy of the Recurring Shopping API.
2. Enter the following command: `curl <baseURL>/users?{searchparameter}="{desiredvalue}"`, replacing the variables to match your system and desired search criteria and press **Enter**.
    * `<baseURL>`matches the URL for the Recurring Shopping API service. In most systems, the URL is `http://localhost:3000`
    * `{searchparameter}` is `firstName`, `lastName`,`email`, or `id`
    * `"{desiredvalue}"` is your search criteria

    **Example** `curl http://localhost:3000/users?lastName="Powell"`

**Result:** The service returns the all entries that match your criteria. If no user matches the search criteria, the service will return an empty array (`[]`)

#### Example `users` object

```json
[
    {
        "lastName": "Powell",
        "firstName": "Alison",
        "email": "alison.powell@example.com",
        "id": "1"
    }
]
```
