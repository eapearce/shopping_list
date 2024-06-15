---
layout: page
---
# Get a list of all users

Returns an array of all [user](users.md) objects in the Reoccurring Shopping service.

## URL

```shell
{server_url}/users
```

## Method

GET

## Params

None

## Request headers

None

## Request body

None

## Return body

```json
{
    "lastName": "Powell",
    "firstName": "Alison",
    "email": "alison.powell@example.com",
    "id": "1"
  },
  {
    "lastName": "Robertson",
    "firstName": "Audrey",
    "email": "audrey.robertson@example.com",
    "id": "2"
  },
...
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | OK | Successful request|
| 404| Not found | Improperly formatted request|

## Tutorial

For help, see the following tutorial: [Searching for users](../tutorial/searching_users.md).
