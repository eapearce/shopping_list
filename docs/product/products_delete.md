---
layout: page
---
# Delete a product

Delete a user. You must specify the `id` of the product in the endpoint.

## URL

```shell
{server_url}/products/{id}
```

## Method

DELETE

## Request headers

This request does not use any authorization. The endpoint is available to all products and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data. | Optional | application/json. Default value.  |

## Request body

None

## Return body

Returns the deleted product.

**Example**

```json
{
    "userId": 3,
    "productName": "Formula milk",
    "storeName": "Amazon",
    "lastPurchased": "2024-04-01",
    "intervalMonths": 1,
    "id": "3"
},
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 200| OK | Successful request.|
| 404| Not found | Improperly formatted request.|
