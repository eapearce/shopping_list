---
layout: page
---

# Recurring Shopping API

The Recurring Shopping API enables users to create and manage lists of products they frequently buy throughout the year.

Administrators can manage users or allow users to subscribe or unsubscribe with a minimum of oversight.

Authentication uses Basic Auth.

Need help? This service has extensive [user documentation](https://eapearce.github.io/shopping_list/).

**NOTE:** This is a mock API to simulate the REST interface of an imaginary service.

## Quickstart

Get started with the following tutorials:

* System setup
* Creating a user
* Adding a new list item

## Authentication

The Recurring Shopping API uses Basic Auth.

Each request must include the username and password encoded in Base64 in the HTTP Authorization header.

## API Reference

Detailed descriptions of the service's resources. The `products` and `users` resources support get, update, patch, delete, and search.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [Users resource](./user/users.md)
* POST user
* GET user
* GET users by property
* UPDATE user
* DELETE user
* [Products resource](./product/products.md)
* POST product
* GET product
* GET product by property
* UPDATE product
* DELETE product

## Tutorials

Learn how to use this service to create, update, and delete users and products.

First, complete this setup tutorial to set up your development system. You only have to do this one time per development system.

* Create a user
* Create a product
* Search for all users or by property
* Search for all products or by property
* Update a user
* Update a product
* Delete a user
* Delete a product

## Troubleshooting and support

See the following topics for help:

* Review environment setup
* Error handling
* [User documentation](https://eapearce.github.io/shopping_list/)
