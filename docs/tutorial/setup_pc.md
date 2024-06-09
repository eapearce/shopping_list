---
layout: page
---
# Tutorial: Local setup for PC

The following instructions describe how to set up your system for local testing on Windows.

For information about how to setup MacOS, see the [MacOS installation guide](setup_macos.md).

## Requirements

Ensure you have the following set up on your development system:

* A [GitHub account](https://github.com)
* [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
* [GitHub Desktop](https://desktop.github.com) (optional)
* A fork of the [repo](https://github.com/eapearce/shopping_list)
* A current/LTS version of [node.js](https://nodejs.org/en/)
* A current version of [json-server](https://www.npmjs.com/package/json-server)
* A current copy of the database file.
* The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Recurring Shopping List** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

Follow these steps to confirm your system is ready:

1. Create and checkout a test branch of your fork of the Recurring Shopping API repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the shopping_list directory in the list)
    cd to-do-service
    git checkout -b tutorial-test
    cd api
    json-server -w recurring-shopping-db-source.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/users
    ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```js
    {
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
    },
    {
    "last_name": "Jones",
    "first_name": "Jill",
    "email": "j.jones@example.com",
    "id": 2
    },
    ...
    ```

If you don't see the list of users, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of users from the service, you're ready to do
the tutorials.
