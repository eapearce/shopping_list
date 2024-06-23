---
layout: page
---
# Get a product by parameter

Returns an array filtered by the designated parameter of all [products](products.md) objects in the Reoccurring Shopping service. You can filter the product list by the following parameters:

* `UserId`
* `productName`
* `storeName`
* `lastPurchased`
* `intervalMonths`
* `id`

## URL

```shell
{server_url}/products/?{parameter}="{desiredvalue}"
```

## Method

GET

## Query Parameters

All parameter values are case sensitive.

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `userID` | Number | The ID of the user resource to which this product is assigned |
| `productName` | String | The products name or short description |
| `storeName` | String | The name of the retailer|
| `lastPurchased` | String | The date the product was purchased in YYYY-MM-DD format|
| `IntervalMonths` | Number | The number of months between purchases of this product|
| `id` | Number | The product's unique record ID|

## Request headers

None

## Request body

None

## Return body

Returns all matching user objects. If no products match your search string, the system returns an empty array`[]`.

**Example**

```json
{
    "userId": 1,
    "productName": "Soap",
    "storeName": "Walmart",
    "lastPurchased": "2024-05-01",
    "intervalMonths": 4,
    "id": 8
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | OK | Successful request |
| 404| Not found | Improperly formatted request |

## Tutorial

For help, see the following tutorial: [Search for a user by parameter](../tutorial/search_user_parameter.md).
