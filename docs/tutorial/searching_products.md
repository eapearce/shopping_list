---
layout: page
---
# Tutorial: Searching for products

You can search products by any of the following criteria:

* `UserId`
* `productName`
* `storeName`
* `lastPurchased`
* `intervalMonths`
* `id`

The service returns only results that match the search parameters exactly.  **Note:** Searching is case sensitive.

## Request format

To search for a specific product, append a question mark (`?`) to `/products` in the URL, followed by the relevant query parameters. The format of the search string is as follows: `<baseURL>/products?=<searchparameter>=<"desiredvalue">`

* To search by a product, add the `productName` parameter to the URL followed by an equals sign (`=`) and the desired product.
* To search by a store, add the `storeName` parameter to the URL followed by an equals sign (`=`) and the desired store.
* To search by a the last purchased date, add the `lastPurchased` parameter to the URL followed by an equals sign (`=`) and the last purchased date inYYYY-MM-DD format.
* To search by user ID, add the `userId` parameter to the URL followed by an equals sign (`=`) and the desired user ID.
* To search by ID of the product, add the `id` parameter to the URL followed by an equals sign (`=`) and the ID.

For a step-by-step tutorial, see [Tutorial: Search for a product by parameter
](search_products_parameter.md).

## Response format

The service returns all associated entries info that matches your criteria. If more than one entry matches your search term, the service will return multiple entries.

If no entry matches the search criteria, the service will return an empty array ([]).
