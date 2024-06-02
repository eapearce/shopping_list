---
layout: page
---
# `products` resource

Base endpoint:

```shell
{server_url}/products
```

The product database contains information about the product users want to purchase.

**NOTE:** You must add a user before you can create your first product.

## Parameters

All parameters are required and are case sensitive.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `userID` | Number | The ID of the user resource to which this product is assigned |
| `productName` | String | The products name or short description |
| `storeName` | String | The name of the retailer|
| `lastPurchased` | String | The date the product was purchased in YYYY-MM-DD format|
| `IntervalMonths` | Number | The number of months between purchases of this product.|
| `id` | Number | The product's unique record ID.|

## Operations

The `products` resource supports these operations.

### READ (GET)

* [Get all product](products_get_all.md)
* [Get product by property](./products_get_parameter.md)

### CREATE (POST)

* [Create product](products_post.md)

### UPDATE (PUT/PATCH)

* [Change product parameter](products_patch.md)

### DELETE

* [Delete product](products_delete.md)
