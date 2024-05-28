---
layout: page
---

# `users` resource

The user database contains information about the users of the service.

**NOTE:** You must add a user before you can create your first product.

## Resource properties

Sample `users` resource

```js
{
    "lastName": "Powell",
    "firstName": "Alison",
    "email": "alison.powell@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `lastName` | string | The user's last name |
| `firstName` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | The user's unique record ID |

## Operations

The `user` resource supports these operations.

### READ (GET)

* [Get all users]
* [Get users by property]

### CREATE (POST)

* [Create user]

### UPDATE (PUT/PATCH)

* [Change user property]

### DELETE

* [Delete user]
