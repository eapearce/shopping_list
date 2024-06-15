# `users` resource

Base endpoint

```shell
{server_url}/users
```

Use this endpoint to create, manage, and delete your users.

**NOTE:** You must add a user before you can create your first product.

**Example `users` object**

```json
{
  "users": [
    {
      "lastName": "Powell",
      "firstName": "Alison",
      "email": "alison.powell@example.com",
      "id": 1
},
```

## Parameters

All parameters are case sensitive.

| Property name | Type | Required | Description |
| ------------- | ----------- | ----------- | ----------- |
| `lastName` | Number | Required | The user's last name|
| `firstName` | String | Required | The user's first name|
| `email` | String | Required | The user's email address|
| `id` | Number | Required | The user's unique record ID|

## Operations

The `users` resource supports these operations.

### READ (GET)

* [Get all users](users_get_all.md)
* [Get users by property](./users_get_parameter.md)

### CREATE (POST)

* [Create users](users_post.md)

### UPDATE (PUT/PATCH)

* [Change user parameter](users_patch.md)

### DELETE

* [Delete user](users_delete.md)
