---
layout: page
---
# Update a user

Changes the value of the specified parameter. You must specify the `id` of the user in the endpoint.

## URL

```shell
{server_url}/users/{id}
```

## Method

PATCH

## Request headers

This request does not use any authorization. The endpoint is available to all products and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data. | Optional | application/json. Default value.  |

## Request body

In the request body, specify the parameter you wish to change and the new value. The following table lists the parameters that you can change.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `lastName` | Number | The user's last name. |
| `firstName` | String | The user's first name. |
| `email` | String | The user's email address.|
| `id` | Number | The user's unique record ID.|

**NOTE:** All parameters are case sensitive.

**Example**

```json
{
"lastName": "Powel",
},
```

## Return body

Returns the updated parameter and the `id`.

**Example**

```json
{
    "lastName": "Powel",
    "id": "1"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 200| OK| Successful update.|
| 404| Not found | Improperly formatted request.|
