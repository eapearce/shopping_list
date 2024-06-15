---
layout: page
---
# Post a new product

Create a new product.

## URL

```shell
{server_url}/products
```

## Method

POST

## Request headers

This request does not use any authorization. The endpoint is available to all products and applications.

| Header name | Description | Required | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data | Optional | application/json. Default value.  |

## Request body

In the request body, specify a JSON representation of the [`products`](./products.md) object. The following table lists the parameters that are required when you create a product.

| Property name | Type | Required | Description |
| ------------- | ----------- | ----------- |----------- |
| `userID` | Number | Required | The ID of the user resource to which this product is assigned |
| `productName` | String | Required| The products name or short description |
| `storeName` | String | Required| The name of the retailer|
| `lastPurchased` | String | Required| The date the product was purchased in YYYY-MM-DD format|
| `IntervalMonths` | Number | Required | The number of months between purchases of this product|
| `id` | Number | Required | The product's unique record ID|

**NOTE:** All parameters are case sensitive.

**Example**

```json
{
    "userId": 1,
    "productName": "Washing powder",
    "storeName": "Amazon",
    "lastPurchased": "2024-02-201",
    "intervalMonths": 3,
    "id": "1"
},
```

## Return body

Returns the product object you created.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 201 | Created | Successful product creation|
| 404 | Not found | Improperly formatted request|

## Tutorial

For help, see the following tutorial: [Creating a product](../product/products_post.md)
