---
layout: page
---

# Before you start

You'll need to complete these steps before you can run the **Who's Working** service quickstart tasks or tutorial.

Expect this preparation to take about 20 minutes to complete.

## Getting ready

The following instructions describe how to set up a system for a Windows machine. To prepare a MacOS machine for the tutorial, visit the MacOS installation guide.

To complete the tutorial, you need the following.

* A [GitHub account](https://github.com)
* A development system (e.g. PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).

You'll need the following software on your development system:

* [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line).
* [GitHub Desktop](https://desktop.github.com) (optional).
* A fork of the [Who's Working service repo](https://github.com/writingteacher/who-working) and a clone on your local machine.
* A current/LTS version of [node.js](https://nodejs.org/en/).
* A current version of [json-server](https://www.npmjs.com/package/json-server).
* A current copy of the database file. You can get this by syncing your fork.
* The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Who's Working service** on your development system with an `http://localhost` hostname, the web version of Postman can't perform the exercises.

**TIP**: If you're using a clone of the repo on your desktop, create a working branch for your tutorial work. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another.

## Testing your development system

To test your development system, follow these steps:

Create and checkout a working branch of your **Who's Working** service clone. Your `GitHub repo workspace` is the directory that contains the `Who's Working` clone. The database file that you need to access in the API folder is called `shift-db-source.json`.

    ```shell
    cd < your GitHub repo workspace >
    ls
    # (see the who-working service directory in the list)
    cd who-working
    cd api
    json-server -w shift-db-source.json
    ```

If your development system is installed correctly, you should see the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

```json
    curl http://localhost:3000/shifts
```

3. If the service is running correctly, you should see a list of shifts from the service, such as in this example.

```js
    [
        {
        "id": "1",
        "date": "2024-06-01",
        "start_time": "0700",
        "shift_length": "4",
        "warning": "opening",
        "location_detail": "Eatons Centre",
        "status": "open"
        },
        {
        "id": "2",
        "date": "2024-06-03",
        "start_time": "1030",
        "shift_length": "4",
        "warning": "none",
        "location_detail": "Yorkville Mall",
        "status": "open"
        },
        ...
    ```

If you don't see the list of `shifts`, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of shifts from the service, you're ready to do the [quickstart tasks](../api/quickstart_working.md) or a [tutorial](update-a-shift.md).
