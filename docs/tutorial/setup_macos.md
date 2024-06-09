---
layout: page
---
# Tutorial: Local setup for MacOS

The following instructions describe how to set up your system for local testing on MacOS.

For information about how to prepare Windows, see the [Local setup for PC](setup_pc.md).

## Requirements

Ensure you have the following set up on your development system:

* A [GitHub account](https://github.com)
* [GitHub Desktop](https://desktop.github.com) (optional)
* A fork of the [repo](https://github.com/eapearce/shopping_list)
* A current copy of the database file.
* The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Recurring Shopping List** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Overview

During the installation process, you will install the following programs:

* [Homebrew](https://brew.sh/)
* [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
* A current/LTS Version of `node.js`
* a current version of [json-server](https://www.npmjs.com/package/json-server)

## Installation

1. Open Terminal.app
2. Paste the following code into terminal and press enter:

    ```shell
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

3. Follow the prompts to complete the Homebrew installation.
4. Paste the following code into terminal and press enter:

    ```shell
    brew install git node json-server
    ```

5. Paste the following code into terminal and press enter:

    ```shell
    sudo npm install -g json-server
    ```

6. Type the following command, with your fork of the GitHub repository in the place of `{Repo}`

    ```shell
    git clone {Repo}
    ```

**Result:** You have completed install. To confirm a successful installation, complete the following procedure: [Test your development system](#test-your-development-system)

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
    [
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
