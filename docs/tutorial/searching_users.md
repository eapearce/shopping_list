---
layout: page
---

# Tutorial: Searching for users

You can search for users by any of the following parameters:

* `firstName`
* `lastName`
* `email`
* `id`

The service returns only results that match the search parameters exactly.  
**Note:** User names and emails are case sensitive.

## Request format

To search for a specific user, append a question mark (`?`) to `/users` in the URL, followed by the relevant query parameters. The format of the search string is as follows: `<baseURL>/users?=<searchparameter>=<"desiredvalue">`

* To search by a specific first name, add the `firstName` parameter to the URL followed by an equals sign (`=`) and the desired first name.
* To search by a specific last name, add the `lastName` parameter to the URL followed by an equals sign (`=`) and the desired last name.
* To search by a specific email, add the `email` parameter to the URL followed by an equals sign (`=`) and the desired email address.
* To search by user ID, add the `id` parameter to the URL followed by an equals sign (`=`) and the desired user ID.

For a step-by-step tutorial, see [Tutorial: Search for a user by parameter](search_user_parameter.md).

## Response format

The service returns all associated user info that matches your criteria. If more than one user matches your search term, the service will return multiple users.

If no user matches the search criteria, the service will return an empty array ([]).
