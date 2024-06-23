---
layout: page
---

# Recurring Shopping API

The Recurring Shopping API enables users to create and manage lists of products they frequently buy throughout the year. After registering, users can create and maintain a list of products they frequently buy, the store they purchase their product from, and how often they purchase it. Users can also specify a buying interval in months with a last purchased date for reminders.

Administrators can manage users directly or allow users to subscribe or unsubscribe with a minimum of oversight.

**NOTE:** This is a mock API to simulate the REST interface of an imaginary service.

## Quickstart

Complete [this tutorial](./tutorial/quickstart.md) to set up your system, create your first user, and create your first product.

## Authentication

This mock service does not use any authorization. The endpoints are available to all products and applications.

## API Reference

Detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they
refer to the URL of a resource. The `{base_url}` value depends
on the installation of the service.

When running a local test, the `{base_url}` is generally `http://localhost:3000`.

* [Users endpoint](./user/users.md)
* [Products endpoint](./product/products.md)

## Tutorials

Learn how to use this service to create, find, update, and delete users and products using Postman.

### System setup tutorial

First, complete this tutorial to set up your development system. You only have to do this one time per development system.

* System setup [PC](./tutorial/setup_pc.md) or [MacOS](./tutorial/setup_macos.md)

### Common task tutorials

These tutorials explain how to accomplish common tasks in the Recurring Shopping API using Postman.

#### Tutorials for users

* [Creating a user](./tutorial/create_user.md)
* [Searching for a user](./tutorial/searching_users.md)
* [Update a user](./tutorial/update_user.md)
* [Delete a user](./tutorial/delete_user.md)

#### Tutorials for products

* [Creating a product](./tutorial/create_product.md)
* [Searching for a product](./tutorial/searching_products.md)
* [Update a product](./tutorial/update_product.md)
* [Delete a product](./tutorial/delete_product.md)

## Troubleshooting and support

Error messages are defined in each endpoint:

* [Users endpoint](./user/users.md)
* [Products endpoint](./product/products.md)

See the following information for help:

* Review environment setup for [PC](./tutorial/setup_pc.md) or [MacOS](./tutorial/setup_macos.md)
* [User documentation](https://eapearce.github.io/shopping_list/)
* [Changelog](changelog.md)
