---
layout: page
---
# Get a list of all users

Returns an array filtered by the designated parameter of all [user](users.md) objects in the Reoccurring Shopping service. You can filter the user list by the following parameters:

* `firstName`
* `lastName`
* `email`
* `id`

## URL

```shell
{server_url}/users/?{parameter}="{desiredvalue}"
```

## Method

GET

## Query Parameters

All parameter values are case sensitive.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `lastName` | Number | The user's last name. |
| `firstName` | String | The user's first name. |
| `email` | String | The user's email address.|
| `id` | Number | The user's unique record ID.|

## Request headers

None

## Request body

None

## Return body

Returns all matching user objects. If no users match your search string, the system returns an empty array`[]`.

**Example response**

```json
{
    "lastName": "Powell",
    "firstName": "Alison",
    "email": "alison.powell@example.com",
    "id": "1"
  },
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | OK | Requested data returned successfully |
| 404 | Not found | Improperly formatted request |

## Tutorial

For help, see the following tutorial: [Search for a user by parameter](../tutorial/search_user_parameter.md)
