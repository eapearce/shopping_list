---
layout: page
---
# `products` resource

Base endpoint:

```shell
{server_url}/products
```

The product database contains information about the product users want to purchase.

**NOTE:** You must add a user before you can create your first product. Products remain after the time specified by "intervalMonths" and are not automatically deleted.

## Resource properties

Sample `products` resource

```js
{
      "userId": 1,
      "productName": "Soap",
      "storeName": "Walmart",
      "lastPurchased": "2024-05-01",
      "intervalMonths": 4,
      "id": 8
    }
```

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

* [Get all product]
* [Get product by property]

### CREATE (POST)

* [Create product]

### UPDATE (PUT/PATCH)

* [Change product property]

### DELETE

* [Delete product]
