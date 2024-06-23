---
layout: page
---
# Post a new user

Create a new user.

## URL

```shell
{server_url}/users
```

## Method

POST

## Request headers

This request does not use any authorization. The endpoint is available to all users and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data | Optional | application/json. Default value.  |

## Request body

In the request body, specify a JSON representation of the [`users`](./users.md) object. The following table lists the parameters that are required when you create a user.

| Property name | Type | Required | Description |
| ------------- | ----------- | ----------- |----------- |
| `lastName` | Number | Required | The user's last name |
| `firstName` | String | Required |The user's first name |
| `email` | String | Required | The user's email address|
| `id` | Number | Required | The user's unique record ID|

**NOTE:** All parameters are case sensitive.

**Example**

```json
 {
    "lastName": "Fake",
    "firstName": "Iam",
    "email": "IamFake@example.com",
    "id": "102"
},
```

## Return body

Returns the user object you created.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 201| Created | Stressful user creation.|
| 404| Not found | Improperly formatted request|

## Tutorial

For help, see the following tutorial: [Creating a user](../tutorial/create_user.md).
