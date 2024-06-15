---
layout: page
---
# Get a list of all products

Returns an array of all [products](products.md) objects in the Reoccurring Shopping service.

## URL

```shell
{server_url}/products
```

## Method

GET

## Parameters

None

## Request headers

None

## Request body

None

## Return body

```json
 {
    "userId": 1,
    "productName": "Washing powder",
    "storeName": "Amazon",
    "lastPurchased": "2024-02-201",
    "intervalMonths": 3,
    "id": "1"
  },
  {
    "userId": 2,
    "productName": "Dog food",
    "storeName": "Amazon",
    "lastPurchased": "2024-04-01",
    "intervalMonths": 1,
    "id": "2"
  },
...
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | OK | Successful request |
| 404| Not found | Improperly formatted request |

## Tutorial

For help, see the following tutorial: [Searching for products](../tutorial/searching_products.md)
