---
layout: page
---
# Update a product

Changes the value of the specified parameter. You must specify the `id` of the product in the endpoint.

## URL

```shell
{server_url}/products/{id}
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
| `userID` | Number | The ID of the user resource to which this product is assigned |
| `productName` | String | The products name or short description |
| `storeName` | String | The name of the retailer|
| `lastPurchased` | String | The date the product was purchased in YYYY-MM-DD format|
| `IntervalMonths` | Number | The number of months between purchases of this product.|
| `id` | Number | The product's unique record ID.|

**NOTE:** All parameters are case sensitive.

**Example**

```json
{
"storeName": "Walgreens",
},
```

## Return body

Returns the updated parameter and the `id`.

**Example**

```json
{
    "storeName": "King Soopers",
    "id": "1"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | -----------|
| 201| Created | Stressful product creation.|
| 404| Not found | Improperly formatted request.|
