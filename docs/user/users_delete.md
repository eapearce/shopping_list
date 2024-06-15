---
layout: page
---
# Delete a user

Delete a user. You must specify the `id` of the user in the endpoint.

## URL

```shell
{server_url}/users/{id}
```

## Method

DELETE

## Request headers

This request does not use any authorization. The endpoint is available to all products and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data | Optional | application/json. Default value.  |

## Request body

None

## Return body

Returns the deleted user.

**Example**

```json
{
  "id": "10",
  "lastName": "Fake",
  "firstName": "Iam",
  "email": "IamFake@example.com"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 200| OK | Successful call|
| 404| Not found | Improperly formatted request|

## Tutorial

For help, see the following tutorial: [Delete a user](../tutorial/delete_user.md).
